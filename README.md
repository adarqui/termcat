Wrote this in 2001, unbelievably still useful. I've had to use this to paste huge urlfilter configs into fortigates. It seems they have some kind of input processing bug.


Redacted original README from 2001:

 XXX  termcat [05/16/2001]               X!x
 XXX   upload files through tty          X!x

 README:

termcat: upload files/crap through a tty that you already have in session.

	...

	This is also good for me who can't scp/upload anything on my
	dialup for god only knows. So here's what I do:


	$ tar zcvf w4r3z.tgz /0d4yw4r3z
	$ uuencode w4r3z.tgz w4r3z.tgz > y0.uu
	$ export TERMCAT=/dev/tty1
	$ export TERMSLP=30000
	$ termcat y0.uu


	NOTE: on /dev/tty1 I am connect to some box via ssh and have issued
	the command: cat > y0.uu. Also note that if you have an el8 connection
	you can set TERMSLP to like, 100 or 0. It will go much quicker with
	lower TERMSLP (TERMSLP is a usleep()).


	somebox$ cat > y0.uu
	somebox$ uudecode y0.uu
	somebox$ tar zxvf w4r3z.tgz
	...
	...

termcat: upload files/crap through a tty that you already have in session.
