# Rsa::Encrypter

Gem is in development-mode

## Developer

Cevin Eichnau

www.eichnau.com

## Installation

Add this line to your application's Gemfile:

    gem 'rsa-encrypter'

And then execute:

    $ bundle

Or install it yourself and require in your ruby file:

    $ gem install rsa-encrypter
    #require "rsa-encrypter"


## Usage

example to use :

generate public and private key 

    key = Rsa::Encrypter.generate_rsa 


or you can set the secure level manualy (1-6), default is 5 (secure but slow) when the secure level smaller than is the encrypter faster but less secure

    key = Rsa::Encrypter.generate_rsa(3)    
    
a sample message to encrypting (m)

    puts "your message ?" 

    print "=> "; m = gets.chomp
    
e is the encrypted message encrypt needs 3 args 1 = message, 2 = public key (key[1]) and 3 =(key[0]) for calculate with public key     

    e = Rsa::Encrypter.encrypt(m, key[1], key[0])

decrypt needs to 3 args 1:mesage, 2:private key (key[2]) and 3: (key[0]) dor calculate with private key

    puts Rsa::Encrypter.decrypt(e, key[2], key[0])

## Time

enter your message

    => ruby
    
decrypted message :

    => ruby
    
time to need for en/decrypting the message  by secure level 6  


    |------------------------------------------------------------|

    Time elapsed encrypt 0.8540000000000001 milliseconds

    |------------------------------------------------------------|

    Time elapsed decrypt 2130.5420000000004 milliseconds

    |------------------------------------------------------------|

    Time elapsed all 2131.4030000000002 milliseconds

    |------------------------------------------------------------|

## Todo

in the next stpes i build tests and a wiki-documentation

