<H4> Launching a Python Flask runtime container</H4>

Go in the required folder (in my case here, the one containing ```flask_example.py```:

```docker run -it --name myflask1 -p 5000:5000


```docker run``` simply start a new container
```-it ``` allows for an interactive container with output in terminal window
```-p 5000:5000``` defines the port mapping. Every container has it own network stack, own IP address, etc... Flask waits for http requests at this defined port (5000). 5000 on the left is Host Port, 5000 on the right side of the column is the container port.
