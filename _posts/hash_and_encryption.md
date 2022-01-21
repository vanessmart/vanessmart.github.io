---
layout: post
---

# Hashing

Black box methodology that translates and disguises input in a 'glunky' output but cannot be reverse engineered (unlike Encryption).


##### *In practice*
*input*                                          *output*
1                                  ->            8vdfb34eionsl
8vdfb34eionsl            ->            ????? (would give a new output and not produce 
                                                               '1' as might be expected. This would have a completely new hash code)



### Collision:
A collision occurs when based on sheer size the sampe output resembles two different inputs.
	*example*
	input
	abc                          ->             24985efjkbsfb934bfskbs
	222222222222      ->             fgrgh49ewouerwpth49hk

These two inputs have different lengths but their outputs are the same length. This means that some hashes can end up being the same simply on the basis of size of the hash. This creates opportunity for a collision to occur.


#### Code usable to validate an application is safe to download from the internet

*(use below to validate what you are downloading is produced and safe from the creator & that you will not be getting some different application than what you are intending to download)*

Notes: This was used to validate Hash for KeePassXC Application


```      

Last login: Mon Jan 3 11:37:18 on ttys000

vanessamartin@macQJ53Q7JVW1 ~ % ls

Applications Movies

Desktop Music

Documents OneDrive - Kudelski Group

Downloads Pictures

Library Public

vanessamartin@macQJ53Q7JVW1 ~ % cd Downloads 

vanessamartin@macQJ53Q7JVW1 Downloads % ls

CA Certificate.mobileconfig enrollmentProfile.mobileconfig

KeePassXC-2.6.6-arm64.dmg googlechrome.dmg

KeePassXC-2.6.6-arm64.dmg.DIGEST

vanessamartin@macQJ53Q7JVW1 Downloads % shasum

^C

vanessamartin@macQJ53Q7JVW1 Downloads % shasum -h

Usage: shasum [OPTION]... [FILE]...

Print or check SHA checksums.

With no FILE, or when FILE is -, read standard input.

  

 -a, --algorithm 1 (default), 224, 256, 384, 512, 512224, 512256

 -b, --binary read in binary mode

 -c, --check read SHA sums from the FILEs and check them

 --tag create a BSD-style checksum

 -t, --text read in text mode (default)

 -U, --UNIVERSAL read in Universal Newlines mode

 produces same digest on Windows/Unix/Mac

 -0, --01 read in BITS mode

 ASCII '0' interpreted as 0-bit,

 ASCII '1' interpreted as 1-bit,

 all other characters ignored

  

The following five options are useful only when verifying checksums:

 --ignore-missing don't fail or report status for missing files

 -q, --quiet don't print OK for each successfully verified file

 -s, --status don't output anything, status code shows success

 --strict exit non-zero for improperly formatted checksum lines

 -w, --warn warn about improperly formatted checksum lines

  

 -h, --help display this help and exit

 -v, --version output version information and exit

  

When verifying SHA-512/224 or SHA-512/256 checksums, indicate the

algorithm explicitly using the -a option, e.g.

  

 shasum -a 512224 -c checksumfile

  

The sums are computed as described in FIPS PUB 180-4. When checking,

the input should be a former output of this program. The default

mode is to print a line with checksum, a character indicating type

(`*' for binary, ` ' for text, `U' for UNIVERSAL, `^' for BITS),

and name for each FILE. The line starts with a `\' character if the

FILE name contains either newlines or backslashes, which are then

replaced by the two-character sequences `\n' and `\\' respectively.

  

Report shasum bugs to mshelor@cpan.org

vanessamartin@macQJ53Q7JVW1 Downloads % shasum -a 256

^C

vanessamartin@macQJ53Q7JVW1 Downloads % shasum -a 256

uytvnurtvrbcerymkuby,

  

  

^C

vanessamartin@macQJ53Q7JVW1 Downloads % shasum -a 256 KeePassXC-2.6.6-arm64.dmg

9dc121bb08f5b46186930ac9ba189553cec2c2ce9688df466e9ce1d9d75fe8c5 KeePassXC-2.6.6-arm64.dmg

vanessamartin@macQJ53Q7JVW1 Downloads % cat KeePassXC-2.6.6-arm64.dmg.DIGEST 

9dc121bb08f5b46186930ac9ba189553cec2c2ce9688df466e9ce1d9d75fe8c5 KeePassXC-2.6.6-arm64.dmg

vanessamartin@macQJ53Q7JVW1 Downloads %```





# Encryption 

Black box methodology that translates and disguises input in a 'glunky' output and is also reverlable ('glunky' output can be used to find the input), i.e. input -> output AND output -> input


##### *In practice*
*input*                                          *output*
1                                  ->            8vdfb34eionsl
8vdfb34eionsl            ->            1



