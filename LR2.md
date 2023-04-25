# Lab Report 2 - Servers and Bugs
## Part 1
### ``StringServer`` Screenshot
<img width="831" alt="image" src="https://user-images.githubusercontent.com/130115948/234169096-4968ad65-f721-4d3d-aa1e-5a595b9f2dfb.png">

### ``/add-message`` Screenshots
<img width="1091" alt="image" src="https://user-images.githubusercontent.com/130115948/234169331-93d1741f-11b7-4807-8571-dc5ab1692923.png">

* Some of the methods that are called are ``.handleRequest()`` and ``.getPath()``
* ``handleRequest()`` takes in the whole url that the user inputs into their web browser and ``.getPath()`` retreives the path which is the part of the domain ``localhost:3000`` in this case
* Both methods' relevent fields change because they are directly corrolated to the given url which in this case is ``http://localhost:3000/add-message?s=How%20Are%20you`` if it were other request ``.getPath()`` would have a completely or perhaphs similar path right after the `3000`, for ``handleRequest()`` only the part after the domain changes since we are dealing with the same domain everytime.
