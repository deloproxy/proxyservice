# The Proxy Swap Service 
Delo Proxy provides a proxy service of decentralized swap of ERC-20 tokens on the ethereum network, including Layer 2, for both limit and stop orders. It provides a easy-to-use web 
interface so that anyone with an ethereum wallet can post a limit or stop order anonymously, and monitor the order status in progress. 
Currently Polygon mainnet is live. Please go to [Delo Proxy](https://deloproxy.org/) for details. 

## How the Proxy Service Works
When Uniswap was first launched, it created a new, permissionless and decentralized marketplace to trade crypto tokens. But there is one problem, namely, 
you do not know exactly what price you will get before you trade, because you always get the market price at the time of execution, which can vary to a wild range depending 
on the market conditions. What if you can setup a limit order, and know exactly how much you will get when you trade? Sometimes, you may also want to place a stop order to 
protect (or benefit) youself from big moves in the markets. With Delo Proxy services, you can do these things easily.

Here is how the proxy service works. 
- Go to [Delo Proxy](https://deloproxy.org/) web site, and connect with your [MetaMask](https://metamask.io/) account. 
- Select the crypto pair you want to trade, and enter the amount and price. Limit order type is used by default. You can also switch to use Stop order type. 
- Click the Send button to send the swap-in amount to the proxy contract. When you use the proxy service for the first time, MetaMask will ask you to approve it first. 
  The token one sends can only be swapped to the predetermined token to the original sender, or transferred back to the sender if canceled. You can cancel your open order anytime befire it's executed. 
- Meanwhile, there is a background program of the proxy service that's monitoring the prices of all the trading pairs against latest market prices on Uniswap. If the market prices
  reaches the limit order's prices, then the contract is executed to do the swap, and the exact swapped out amount as calculated from the price of the limit order is 
  sent to the original sender (stop order is a little bit more complex, but it follows the same principle).
- The contract is designed in such a way that nobody (incl. contract owner) can directly withdraw tokens from it. The only ways tokens can be transferred out are either through 
  execution of swap or with order being canceled. 
