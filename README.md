# SHA512KDF
#### Description
Derive keys with SHA512 in a webbrowser using JavaScript.

I've created this small project to have a fallback method of computing
some of my passwords in order to access my data in case I do not have
access to my devices.

#### Specification
A given salt and master key are concatenated and the SHA512 sum of the
combined string SHA512($salt + $key) is calculated.

#### Usage
Enter masterkey and salt/service name to obtain derived key.

#### Requirements
- **Minimalistic:** I need to understand (and trust) the code within
  minutes so I can use it without concern. I am going to sign
  all commits but can't rely on remembering the correct GPG-key
  id.
- **Platform independant:** This is necessary as I do not know which
  type of machine I am going to use if/when I am in need of
  a KDF. 
- **Widely accessible:** It should be available anytime and anywhere
  in the world.


#### Note
Using SHA512 as a KDF is bad practice in general! There are better options
out there, like scrypt or Argon2. However, these are not so widely
available, which means I had to use these files even on Linux devices
where utilizing locally installed programs might be a better option.
Do not even bother using this if your master key does not have
sufficient entropy!


#### Possible Features for Future Extensions
- Onscreen keyboard for input using the mouse; possibly with shuffled keys
- Copying derived key to clipboard instead of printing it on the screen.
	Maybe with an option for the user to choose between copying and printing.
