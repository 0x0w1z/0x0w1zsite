---
title: "NCA-CTF I <3 Charmander"
date: 2024-09-29
draft: false
Tags:
  - NCA-CTF
  - Writeups
---

This challenge was Simple forensics challenge which i created for the NCA-CTF where players were given an image which was corrupted and the flag was hidden in there.

To solve this challenge, the approach which i would have taken will be like this firstly, i would try to open the image which will give something like this.

![](1.png)

So, what it tells us that it's not a png file but it shows us it's a png file so, there is something which is done with the header of the image. I would try to open the image in the hex editor i prefer **GHEX** after opening the file in ghex what we can see is this.

![](2.png)

There is something wrong with the header of the file it should have to be different, what it should've looked like would be like this one.

![](3.png)

So, there is a difference in the picture which was given in the challenge and the picture which was the real **PNG** file so, to solve this problem i would change the header using **GHEX** editor to the default value of the **PNG** file. After changing the header of the file to the default values it gives us the original picture where i hide the flag.

![](4.png)

As we can see the picture which we get from the output, we can see there is something written in the body of the charmander.

![](5.png)

That's where i hide the flag if we zoom in there we can see the flag clearly.

Flag : `NCA{D1D_y0u_kn0w_ch4rm4nd3r_is_fire_type}`
