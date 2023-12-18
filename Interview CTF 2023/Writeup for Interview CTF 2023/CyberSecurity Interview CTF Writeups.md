# <center> CyberSecurity Interview CTF Writeups</center>

## 1. **HEIL**
\- By Sahiba

This CTF was the first challenge provided. It goes as follows:

CTF - 

![](images/image.001.png)


HINT- 

![](images/image.002.png)

Now, as the hint suggests, we need to use Caesar cipher to solve this CTF. So, I opened Cyberchef and pasted this CTF there and applied Caesar cipher tool, namely ROT13. I used ROT13 because in the hint the format of the flag is given as GDSC_CTF{} and in the CTF text some gibberish text in that format is present. ROT47 was not my preference because it would have shifted all the special characters too which would disturb the format of my flag. So, I applied ROT13 on it and it did not result in the flag.

![](images/image.003.png)

After checking the hint again, the word `WEEK` was printed in caps and it clicked me to change the rotation amount and enter 7 and see the results.

![](images/image.004.png)

It again did not result in the flag. So, I entered it in with a negative sign and it worked. I found it to be:

```txt
gdsc_ctf{shift_happens}
```

![](images/image.005.png)





## 2. **MindROT**
\- By Jaskaran

CTF Text

![](images/image.006.jpeg)

readme.txt

![](images/image.007.jpeg)

**Solution -**

First thing I do when I see a bunch of gibberish text is to put it in the boxentriq cipher identiﬁer, upon doing that

![](images/image.008.jpeg)

the website returns an unknown format, after this I went through the ieadme.txt, now looking at the title of the ctf as well as reading ‘deﬁnitely ROT away’ made me think that the cipher is a Rot cipher(which is a type of keyboard shift cipher) of some kind, so the next step according to me was to run it through iot13 and iot47, once

![](images/image.009.jpeg)

I put it through rot 13 the text came out to be a bunch of gibberish and to my naked eye didn't look like a cipher I could recognize, so I ran it through rot 47 and that returned something interesting, the text was gibberish but there was an = sign at the end of it which usually points to base64,

![](images/image.010.jpeg)

next thing I did was put it through a base64 decoder, and the text was still gibberish here but there were {,}s present which are also present in our ﬂag format,

![](images/image.011.jpeg)

![](images/image.012.png)so to investigate it further, I put the text in a cipher identiﬁer tool and it urged me to investigate into rot13,

which was on brand for my suspicions since I thought that the level will be ROT based, upon putting the text in a rot 13 decoder, the ﬂag was there, clear as day in front of us.

![](images/image.013.jpeg)


## 3. STRINGS GIBBERISH

### METHOD 1

\- By Gurnoor

**CTF-** [Click Here](https://drive.google.com/file/d/1l0KgPZIHZ9HjtoZAaipxluOH4k2-GzzI/view?usp=drive_link)  



**HINT** - 

```
Can you try to find out the flag from all this gibberish? 
```


Here's a clue: 
``` 
"What's in a name?" - Shakespeare 

Happy Hunting (winkies) 

P.S. The flag format is GDSC_CTF{} 
```


1. I initiated my search for the flag by first directing my attention to “winkies” but unfortunately it proved to be unrelated to the flag. 

2. I reviewed the file thoroughly to notice that title said “strings” gibberish which pointed me to the strings feature in cyberchef. 



![](images/image.015.jpeg) 



3. No differences were spotted between the input and the output. Consequently, I chose to explore the features available to us on cyberchef.
4. The ‘display total’ and ‘sort’ features were not of much assistance as anticipated and the outcome I obtained after the application of these was as follows.

![](images/image.016.png)

5. I could successfully locate the flag after the utilization of the ‘unique’ feature.
6. The flag was ‘GDSC\_CTF{HeY\_yOu\_goT\_THE\_FLaG}’ 

![](images/image.017.jpeg)



### METHOD 2 
\- By Maihere Singh

1. In the given problem, initially I realized that there was a format of text repeating itself again and again

![](images/image.018.png)

So, I thought of removing the other repeated text and concentrate on this one paragraph only, but it seemed to be a bad idea because the flag was nowhere to be seen.

2. I shifted to the whole file and simply pressed Ctrl+F to search the initials of the flag i.e. GDSC_CTF.

   ![](images/image.019.png)

And we got the flag!

The alternate method of solving the challenge could be:

3. Opening the file in linux

4. Searching for the initials of the flag i.e. GDSC_CTF by using grep command.

But this was not necessary in our case, as the given file was in .txt format which made the task even easier.

```text
CTF_Flag: GDSC_CTF{HeY_yOu_goT_THE_FLaG}
```


## **4. Invisible Ink**
\- by Rudra Nautiyal

Steganography, the art of hiding information within other data, has been a timeless technique employed by cryptographers to transmit secret messages discreetly.

"Invisible Ink" makes use of this concept by presenting participants with an image that appears to be nothing more than a digital canvas.

Let take a look at the picture!

![Alt text](images/clip_image001.jpg)

The hint for the same being,

```text
It is hidden just like the one piece.

But not in a place as harsh as the Grand Line. Maybe it's all about our own character?

P.S. The flag format is GDSC_CTF{}
```

Oh no, we've just abandoned our pirate persona, and now they're asking us to revive it? This can't be happening; we need to resolve this situation promptly.໒(⊙ᴗ⊙)७✎▤

If you've had the opportunity to review the initial PDF document provided, the process for extracting the flag is straightforward.

- Open the image file using Notepad.

- Execute a `Ctrl+F` command to initiate the find function.

- Conduct a search specifically for the flag labelled as GDSC_CTF.

This step-by-step approach ensures a systematic exploration of the image file's contents, making it easier to locate and identify the desired flag within the given context.

Let’s take a look now.

![Alt text](images/clip_image003.png)

Opening in Notepad and then searching for the flag we get .

![Alt text](images/clip_image005.png)

Yay, we found the flag, it’s 

```
G D S C _ C T F { g o o d _ g o i n g _ f i n d _ m o r e f l a g s _ i f _ y o u _ h a v e n t _ a l r g g s & g o o d l u c k _ : p }
```

Great job! Nowhere as difficult as finding the ONE PIECE.(⌐■_■)

## **5. Cryptic Wave**
\- by Hargun Kaur

This was the most interesting and fun CTF for me.

CTF:

![Alt text](images/clip_image007.png)

Flag text:

![Alt text](images/clip_image009.png)

For this, I had a hunch that this one would not be solved like the others and I probably needed to download something for this. This suspicion of mine was confirmed by a member of GDSC Cyber security. After doing some research, I discovered that this was a case of Audio Steganography I then downloaded the Sonic Visualiser application and opened the given cryptic.wav file with the app.

![Alt text](images/clip_image011.png)

This looked both very cool and overwhelming as I did not know how to use the application. So I decided to just play around with the features. I stumbled upon the Pane dropdown menu. I tried out the features one by one where the "Add Waveform" feature did nothing but duplicate the already given waveform but just in a different colour.

![Alt text](images/clip_image013.png)

Then I did `Ctrl+Z` to undo the Waveform addition and I tried out the “Add Spectogram” feature.

![Alt text](images/clip_image015.png)

It gave me the following output:

![Alt text](images/clip_image017.png)

I changed its colour from the interactive dropdown menu on the right and got the following flag:

![Alt text](images/clip_image019.png)

Flag:

```
GDSC_CTF{you_found_another_flag_heres_this_W_4_u_xD}
```

  

## **6. Multilingual Mystery**
\- by Jaskaran Singh

CTF Text

![Alt text](images/clip_image021.png)

readme.txt

![Alt text](images/clip_image023.png)

## **Solution –**

After I read the CTF text, going by experience when a text is repeated it usually ends up being Binary or Morse, then I went through the readme.txt but that put me very o track because I knew that I had to focus on “ :\=\==) ” but wasn’t really sure what to make of it, another thing that the readme made clear was that it will require more than one transformations, so my first step of action is to put it in boxentriq’s cipher identifier even though the '=' at the end of the text made it somewhat evident that it might be base64,

![Alt text](images/clip_image025.png)

all it did was confirm my suspicions,

Then decoding it using base64, I got dashes and dots and owing to my previous suspicions I figured it to be Morse Code, Upon getting the morse code, I used boxentriq’s morse code to text converted and all it gave was a bunch of 0s and 1s which was very clearly binary,

![Alt text](images/clip_image027.png)

now using a basic Binary to Text converter all I got was gibberish

![Alt text](images/clip_image029.png)

putting the text into dcode’s cipher identifier , it suggested me to investigate rot47

![Alt text](images/clip_image031.png)

and upon decoding it using dcode’s rot47 decoder, I got a bunch of numbers spaced out which were very clearly decimal codes,

![Alt text](images/clip_image033.png)

now putting it into a decimal-to-text converter, gave me a bunch of plain text which putting it into the flag’s format gave us the answer to the CTF

![Alt text](images/clip_image035.png)

**Flag** –

```
Let’s make this a bit trickier…
```
  


## **Boss Challenge**
\- Written by: @Sahiba Kaur Sethi

CTF 

![image 1](https://github.com/dsc-gtbit/Cybersecurity/assets/140737702/2d8632d3-95e3-47bc-9d54-ade71a82095b)

Readme.txt

![image 2](https://github.com/dsc-gtbit/Cybersecurity/assets/140737702/fbd575cd-9395-4ab7-987c-dd25db27557a)

![image 3](https://github.com/dsc-gtbit/Cybersecurity/assets/140737702/d76f5173-a66e-4465-bc05-7f6d617c8e53)

Context
The boss challenge was another CTF provided by the GDSC team to the participants to test their knowledge, skills and research abilities. Only this time this CTF came with some bigger twists. Anyone who would have solve the CTF would be directly welcomed to the team without any interview or other selection procedures. As exciting and interesting it sounds, it took a lot of research work still the flag was not found. Let us go through the CTF and start solving it.

## **Solution-**

This image was provided and the data hidden in the image was to be found but the only twist was that the key flag found from this image was to be used to find the main flag using the readme file.

After analysing the image I noticed that there were some dots present in different colours on the top left of the image.

![image 4](https://github.com/dsc-gtbit/Cybersecurity/assets/140737702/94526093-3944-47be-8d24-88466f800c39)

After reading the readme file it was sure that these dots were the points on the graph and somehow some graphical outputs were to be considered. Firstly, I uploaded this image file on exif.tools to find the metadata and see if the flag was hidden in the image’s data but no flag or other useful information was found which is obvious as the boss challenge would not give any direct output.

![image 5](https://github.com/dsc-gtbit/Cybersecurity/assets/140737702/27b6850a-a1b8-4e7b-bbc8-ccee1577b415)

A little bit of research on google, it suggested to find the pixels of the image using a python code using the PIL library. 

![image 6](https://github.com/dsc-gtbit/Cybersecurity/assets/140737702/075b3c17-10a6-4f23-9682-dee55a3ca830)

![image 7](https://github.com/dsc-gtbit/Cybersecurity/assets/140737702/a5451839-a470-4656-8f23-daf705329d04)

The output gave me the RGBA values but it was of no use as my next step could be converting them to ASCII values but all these numbers exceeded the character range of ASCII values so it was of no use. I also tried to convert this unsigned ASCII to the signed one and then use it but it still did not give any valued outcome. I tried various new methods for 2-3 days but nothing seemed to work. On reading the readme file again it hit me that I missed one part of the hint provided which was that the oldest and the most unused application come handy in viewing pictures and I thought of using paint to find out any information it could provide. On implementing grid lines and moving the cursor over the points I could read the coordinates. 

![image 8](https://github.com/dsc-gtbit/Cybersecurity/assets/140737702/ee6dfc2d-bd00-48c3-81c1-73ea1640dd8b)

I made a list of all these points and then converted the ascii values to text and the output was still jumbled and not in proper form.

![image 9](https://github.com/dsc-gtbit/Cybersecurity/assets/140737702/07938231-92e0-43a7-accb-14e18f139b98)

On arranging these values in ascending order and converting into text the key flag was found to be “GDSC{LBTGQ_Lights_hehe}”.

![image 10](https://github.com/dsc-gtbit/Cybersecurity/assets/140737702/4d50c4f2-b36e-4c8a-8404-ee22a5af42e1)

This key flag was then supposed to be used to solve the main flag. On applying the AES decryption on the main flag and the key flag using cbc mode of decryption the main flag was found to be “GDSC_CTF{This_is_what_counts}”.

![image 11](https://github.com/dsc-gtbit/Cybersecurity/assets/140737702/d9c2c8a4-5ba1-4e1b-b358-c174228191c3)
 
Many new types of decryption tools and methods were explored while solving the Boss Challenge. it was quite interesting and broaden the thinking and researching techniques.

**Flag**-

```
GDSC_CTF{This_is_what_counts}
```
