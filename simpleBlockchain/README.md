**simpleBlockchain**<br>
This project is really simple blockchain which uses python.<br>
<br>
Use postman(https://www.getpostman.com) to query GET/POST to server.<br>
<br>
**http://{node}/nodes/register** [POST]<br>
Register server with different ports as http://127.0.0.1:5001/nodes/register, http://127.0.0.1:5002/nodes/register.<br>
The body should be JSON format as { "nodes": [ "http://127.0.0.1:5002" ] }.<br>
<br>
**http://{node}/mine** [GET]<br>
Create new block with transaction list for mine that will be added to chain.<br>
<br>
**http://{node}/chain** [GET]<br>
Check blocks that added to the chain on the current node.<br>
<br>
**http://{node}/nodes/resolve** [GET]<br>
The longest chain on the all nodes will be selected.<br>
If the chain on the other node is selected, the existing chain will be replaced.<br>
<br>
**http://{node}/transactions/new** [GET]<br>
New transaction is created and it will be added to current block. When /mine is called, the block will be added to chain.<br>
<br>