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







# Encryption 

Black box methodology that translates and disguises input in a 'glunky' output and is also reverlable ('glunky' output can be used to find the input), i.e. input -> output AND output -> input


##### *In practice*
*input*                                          *output*
1                                  ->            8vdfb34eionsl
8vdfb34eionsl            ->            1



