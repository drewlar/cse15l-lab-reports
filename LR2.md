# Lab Report 2 - Servers and Bugs
## Part 1
### ``StringServer`` Screenshot
<img width="831" alt="image" src="https://user-images.githubusercontent.com/130115948/234169096-4968ad65-f721-4d3d-aa1e-5a595b9f2dfb.png">

### ``/add-message`` Screenshots
<img width="1091" alt="image" src="https://user-images.githubusercontent.com/130115948/234169331-93d1741f-11b7-4807-8571-dc5ab1692923.png">

* Some of the methods that are called are ``.handleRequest()`` and ``.getPath()``
* ``handleRequest()`` takes in the whole url that the user inputs into their web browser and ``.getPath()`` retreives the path which is the part of the domain ``localhost:3000`` in this case
* Both methods' relevent fields change because they are directly corrolated to the given url which in this case is ``http://localhost:3000/add-message?s=How%20Are%20you`` if it were other request ``.getPath()`` would have a completely or perhaphs similar path right after the `3000`, for ``handleRequest()`` only the part after the domain changes since we are dealing with the same domain everytime.

<img width="1046" alt="image" src="https://user-images.githubusercontent.com/130115948/234170274-024bea06-3239-46a2-a933-c8e7ce1b8643.png">

* Some other methods that are called here are the ``String.format()`` and ``.getQuery()``
* ``String.format()`` takes in the what is in ``message``, in this case ``"How Are you \n I Am doing very fine thank you for asking :) \n"`` and sets it up to be able to print out on the web server in ``localhost:3000``. ``getQuery()`` gets the part of the URL starting at ``?`` which indicates the start of a query.
* Both methods change depending on what is sent through the query part of url, in this case ``String.format()`` would return a completely different set of words if the query is changed, ``.getQuery()`` would change according as well


## Part 2
### Failure-inducing input
```
@Test 
  public void testSumEvensLength4()
  {
    int[] input1 = { 12, 13, 7, 2};
   assertEquals(EvensExample.sumEvenIndices(input1), 19);
  }
```
### Failure free input

```
@Test
  public void testSumEvenLength6() {
    int[] input1 = { 12, 13, 7, 8, 5, 3};
    assertEquals(EvensExample.sumEvenIndices(input1), 24);
  }
}
```
### Symptom

<img width="1104" alt="image" src="https://user-images.githubusercontent.com/130115948/234173306-082b59a2-c67b-40ab-a442-e2a93a035a1f.png">

### Before-After Bug
#### Before
```
class EvensExample {
  static int sumEvenIndices(int[] nums) {
    int sum = 0;
    for(int i = 0; i < nums.length; i += 2) {
      sum += nums[i + 1];
    }
    return sum;
  }
}
```
#### After
```
class EvensExample {
  static int sumEvenIndices(int[] nums) {
    int sum = 0;
    for(int i = 0; i < nums.length; i += 2) {
      sum += nums[i];
    }
    return sum;
  }
}
```
The only thing needed to be changed was the index of which sum was getting its value from, in the before the method was grabbing every even number but not the even index (remember index starts at 0 not 1), thus the before code was actually getting all the odd indices. With this change it is now starting at the 0th index and then going through every even index


## Part 3
To me websites seemed something way beyond my grasp of knowledge, I thought I neeeded a very indepth knowledge of how data is transfered in and out of servers and how to set up the actuall display. I learned from lab 2 that it is somewhat easier than I thought, I learned that I can create my own local server and enter my own website, this is pretty cool because I wonder if I can create some methods / systems that could help me in my HW, or perhaps I can set up the page on my UCSD accound then have a chat based website with my Peers. Lab 2 brought a small glimpse on how servers and websites work, I hope I could use this in the near future for fun :).
