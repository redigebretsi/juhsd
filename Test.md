---


---

<h1 id="peer-to-peer-crypto-currency-protocol">Peer to peer crypto currency protocol</h1>
<h2 id="protocol-descriptiontracker-side">Protocol description:Tracker side</h2>
<h2 id="section"></h2>
<ul>
<li>INITIALIZE: a new miner will initialize the request to obtain the list of other miners to the tracker.<br>
-ACCEPT REQUEST: listing server or tracker will accept the request of the new miner.</li>
<li>SEND LIST: tracker will send the list of available miners.</li>
<li>WAITING: the new miner will wait for the response from the tracker.<br>
Case1: if the miner doesn’t receive any response within 30sec(say for ex), it goes to the timeout state.<br>
Case2: in case of a loss, the miner will again send the request to the tracker.</li>
<li>ACCEPT LIST: miner accepts the list send by the tracker.</li>
<li>ACKNOWLEDGE LIST: the new miner will send an acknowledgement to the listing server or tracker.</li>
<li>ACCEPT ACKNOWLEDGE: after receiving the acknowledgement from the miner, the tracker will update the new miner to the list of miners.</li>
</ul>
<h2 id="protocol-description-miner’s-side">Protocol description: Miner’s side</h2>
<p>All your files and folders are presented as a tree in the file explorer. You can switch from one to another by clicking a file in the tree.</p>
<h2 id="stage1-before-mining">STAGE1: Before Mining</h2>
<ul>
<li>PUSH TRANSACTION: transaction send by the user</li>
<li>ACCEPT TRANSACTION: only one miner will accept the transaction</li>
<li>TRANSACTION: Initial miner will share it with other miners</li>
</ul>
<h2 id="stage2-mining">STAGE2: Mining</h2>
<ul>
<li>Every miner will try to find the correct hash function for the initial transaction send by the user. Only one of the Miners will generate the correct hash function</li>
<li>HASH BROADCAST: the generated hash will be broadcasted to other miners</li>
<li>VALIDATION: the other miners will validate the hash by checking the previous hash function of the transaction</li>
<li>GENERATEBLOCK: Once the hash is validated, a new block for the transaction is generated.</li>
</ul>
<h2 id="stage3-communication-between-the-existing-miners">STAGE3: COMMUNICATION BETWEEN THE EXISTING MINERS</h2>
<ul>
<li>CONNECT: every miner connects to every other miner and make sure that they exchange the blocks (transactions)if any of the miner has more or less than the other.</li>
<li>SEND REQUEST: if any of the miner has less blocks(transactions)it will request other miners for the blocks(transactions).</li>
<li>RECEIVE BLOCK: the miner which requested for the block(transactions) will receive the block(transactions) send by another miner.</li>
<li>VALIDITY CHECK: The miner will check whether the received block (transaction) is valid or not</li>
</ul>
<h2 id="stage4-adding-a-new-miner-in-the-block-chain">STAGE4: ADDING A NEW MINER IN THE BLOCK CHAIN</h2>
<p>`</p>

