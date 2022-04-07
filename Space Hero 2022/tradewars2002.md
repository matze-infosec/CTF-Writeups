>> Tradewars2002 -> Space Heroes
>> Matze

**** INFO ****

"Have you tried tradewars2002? You should try tradewars2002!"

Notes: The flag format was not your standard (The!s_!s_@_Fl@g) format that most of the flags where in.

How many colonists were moved from fuel ore production to organics production? Keep in mind a group of
colonists is 1000 colonists. Wrap in shctf{} (ex: shctf{31337})

Setup:

 This challenge was set up very simply. It has you download a pcap file. As soon as you open it a lot of
Telnet data can be seen.

Exploration:

 By using wire shark we are able to follow the TCP stream to see what looks like game logs. I will be
honest, I fell down the rabbit hole of trying to log in to the server using the username of the creator
that where left in the logs. It took a message to the owner to find out that I was wasting my time
with an impossible challenge and got reminded of the flag format.  

Steps to victory:

  After realizing that the answer had to now be in the game log I was looking at I knew I had to clean
up the data. The game log is filled with time marks. example:

.[32mFuel Ore.[1;33&nbsp;m 18,208.[0;31&nbsp;m 3.[1;34&nbsp;m 3,930.[36&nbsp;m 100,000.[0;35&nbsp;m 

I was able to remove a lot of the time marks with a text editor to get a much easier idea of this log.
You start to see a pattern or picking up colonists from one planet, and dropping them off in another.
During this drop off they trade task from ore production to fuel production. We are now able to see the
data required to solve this pop up.

Sweet victory:

 From this point we have everything needed to solve this. We have 2 ways to solve this. One way is to
count by hand. We see that on each trip they move 150 groups per trip. You can count the number of
trips, and multiply that by the 150 groups moved.

 Trips x groups x 1000 = flag

That is a lot of counting, so let's do this the smart way. If we take the starting number for oil
production and find the difference we get our first number. We can do the same thing with organic
production to find our second number. Doing this method we end up with a range.

 18148000 to 18152000

The flag can only be one number so let's take the middle ground on this and call it 18150000. We need to
wrap it in the flag format to make it usable. We end up with the awns er of:

 shctf{18150000}

This did come out to be the flag. I do have a few things I would recommend to the maker. The server
used to capture the challenge was an active server used by a live community of players for the game.
The data left in this challenge coused a lot of trouble for them. This was not done to hurt them, but I
do feel bad for the community effected by it. The flag format was also one of the other killers to this.
I talked to a lot of people after the fact that got so hung up looking for data that matches the other
flags that they never realized they had everything they needed. The challenge was still super fun to
play, and makes me really want to play the game for myself. I look forward to seeing what they bring
next year!
