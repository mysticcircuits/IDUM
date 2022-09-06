//////////////////////////////////////////////////////////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
//////////////////////////////////////////////////////////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

          _____                    _____                    _____                    _____          
         /\    \                  /\    \                  /\    \                  /\    \         
        /::\    \                /::\    \                /::\____\                /::\____\        
        \:::\    \              /::::\    \              /:::/    /               /::::|   |        
         \:::\    \            /::::::\    \            /:::/    /               /:::::|   |        
          \:::\    \          /:::/\:::\    \          /:::/    /               /::::::|   |        
           \:::\    \        /:::/  \:::\    \        /:::/    /               /:::/|::|   |        
           /::::\    \      /:::/    \:::\    \      /:::/    /               /:::/ |::|   |        
  ____    /::::::\    \    /:::/    / \:::\    \    /:::/    /      _____    /:::/  |::|___|______  
 /\   \  /:::/\:::\    \  /:::/    /   \:::\ ___\  /:::/____/      /\    \  /:::/   |::::::::\    \ 
/::\   \/:::/  \:::\____\/:::/____/     \:::|    ||:::|    /      /::\____\/:::/    |:::::::::\____\
\:::\  /:::/    \::/    /\:::\    \     /:::|____||:::|____\     /:::/    /\::/    / ~~~~~/:::/    /
 \:::\/:::/    / \/____/  \:::\    \   /:::/    /  \:::\    \   /:::/    /  \/____/      /:::/    / 
  \::::::/    /            \:::\    \ /:::/    /    \:::\    \ /:::/    /               /:::/    /  
   \::::/____/              \:::\    /:::/    /      \:::\    /:::/    /               /:::/    /   
    \:::\    \               \:::\  /:::/    /        \:::\__/:::/    /               /:::/    /    
     \:::\    \               \:::\/:::/    /          \::::::::/    /               /:::/    /     
      \:::\    \               \::::::/    /            \::::::/    /               /:::/    /      
       \:::\____\               \::::/    /              \::::/    /               /:::/    /       
        \::/    /                \::/____/                \::/____/                \::/    /        
         \/____/                  ~~                       ~~                       \/____/    



  v.95 - Written by Eli Pechman

  This code is released under a Creative Commons Attribution-ShareAlike 4.0 Licence

  https://creativecommons.org/licenses/by-sa/4.0/legalcode

//////////////////////////////////////////////////////////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
//////////////////////////////////////////////////////////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

  Here it is folks, this is the code used in the IDUM Eurorack module sold by Mystic Circuits.  For a good
  overview of this module and how it works check out the product website at:

  www.MysticCircuits.com/product/idum

  In short IDUM works as a sort of multi-fx processor for gates that turns your patterns effortlessly into IDM.  It can add little bits of 
  variation to incoming patterns or it can completely destroy everything going through it.  It also does some fairly complex clock manipulation 
  to an external sequencer allowing you to make it run backwards, loop subsections of the sequence etc.

  I did a my best to make this code as simple to understand and as human-readable as possible.  From the beginning I wanted this module to be as
  easy as possible for people to hack even if they are just messing with a few numbers or changing the under-the-hood options on this page to
  slightly tweak how the module works.  Using the arduino environment felt like a good choice because it is designed to be beginner friendly,
  it is extremely well documented and widely used and therefor easily searchable, and it is easy to install the necessary programs to update your board.

  Please understand that although I am doing my best to encourage people to tweak your IDUM code that doing so can damage your module, especially
  if you reassign pins that are inputs to outputs or vice versa.  Also keep in mind that if you contact me with questions I will do my best to
  answer them but that I am under no obligation to help you alter this program.  Mystic Circuits is a small company and I do not have a lot
  of free time.  Please be patient for me to respond and keep in mind the nicer you ask me for help the more enthusiastic I will be to help.

  If you have suggestions for improvements that can be made or things that can be commented/ explained more clearly in here please do not
  hesitate to get in touch with me through the contact page on my website. I'm not great with Github and I don't check my messages here that
  often so the website is the best way to get a hold of me.  I make no claims to being a great programmer and will not be offended if you tell 
  me a better way to do what I am doing here.
  
//////////////////////////////////////////////////////////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
//////////////////////////////////////////////////////////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\                                                                                                  
   
  Hi Uli!  I know there's not much that I can do to stop you or someone else from using this code or my hardware in their products.  All I'll 
  say is that if you or anyone else ends up using anything here in a way that makes you money please try to: 
  
  a) Change things enough so that your product/ device is different enough from and doesn't compete with IDUM.
  
  b) Try to send some love my way (I'd love a reel of bucket brigade chips).

  If you the reader are at all unsure about whether something will step on my toes again do not hesitate to contact me through my contact form
  on my website.
 
//////////////////////////////////////////////////////////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

   TO DO:

   increase resolution of loop recording and playback
   add 16 step code for looping and maintain cycle functions
   improve slow clock mode reliability and reducing number of triggers when a lot of follow steps are added.
   add split mode
   add code to save loops between power downs

//////////////////////////////////////////////////////////////////////////\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
