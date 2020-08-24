**********To change the default python version:

1)first install the python version you want to update to

2)By entering below code - you will see all the alternatives of python with priority orders(Higher number is given first priority by default)

praneeth@Praneeth-PC:~$ sudo update-alternatives --config python
There are 3 choices for the alternative python (providing /usr/bin/python).

  Selection    Path                Priority   Status
------------------------------------------------------------
* 0            /usr/bin/python3.7   4         auto mode
  1            /usr/bin/python2.7   3         manual mode
  2            /usr/bin/python3.6   2         manual mode
  3            /usr/bin/python3.7   4         manual mode

Press <enter> to keep the current choice[*], or type selection number: 

3)Then add the newly download python version to the alternatives, by adding highest priority number at the end.

Enter: sudo update-alternatives --install /usr/bin/python python /usr/bin/<python version><space><priority number you want to give it>


**********For any further assistance look at the screenshots**********

-----------------Topic related-----------
1) Press 'Cntrl + D' to exit the python interactive shell



**************OTHER*************
1)Your terminal won't be opening if you have any issue with python or you have mistakenly deleted any python version.
However, you can open terminal again from file explorer.

2) Some python packages need to be installed using sudo apt install python3-<package name>
ex: 1) sudo apt install python3-opencv
    2) sudo apt install python3-tk
    3) sudo apt install python3-pip