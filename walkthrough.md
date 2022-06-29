**Gandalf The Wise writeup by Vintage.exe**
			***29.06.2022***

So there we got a png file. Doing binwalk showed its a jpeg image data which means it is actually compressed! But after simply checking file by file command there are 3 comments, encrypted. Let's wake up the cyberchef. 

***Q1RGbGVhcm57eG9yX2lzX3lvdXJfZnJpZW5kfQo=*** is basically base64 ===> CTFlearn{xor_is_your_friend}

So the first comment is basically a hint for our next move. But first, what is xor?
In cryptography xor is simply an encryption algorithm that operates on specified rules. The most important thing to remember is that we use a key to encrypt our message. 
***xD6kfO2UrE5SnLQ6WgESK4kvD/Y/rDJPXNU45k/p*** ===> encypted message?
***h2riEIj13iAp29VUPmB+TadtZppdw3AuO7JRiDyU*** ===> key?

After a while i figured out that cyberchef is all i need and no script is obligatory.
As I suspected, second comment was key indeed and when added two functions (base64 and XOR with key as a second comment) I was able to retrieve the flag.


**CTFlearn{Gandalf.BilboBaggins}**