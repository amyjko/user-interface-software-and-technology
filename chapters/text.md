Just as pointing is a nearly ubiquitous form of _non-verbal_ communication, text is a ubiquitous form of _verbal_ communication. Every single character we communicate to friends, family, coworkers, and computers&mdash;every tweet, every Facebook post, every email&mdash;leverages some form of text-entry user interface. These interfaces have one simple challenge: support a person in translating the verbal ideas in their head into a sequence of characters that are stored, processed, and transmitted by a computer.

If you're reading this, you're already familiar with common text-entry interfaces. You've almost certainly used a physical keyboard, arranged with physical keys labeled with letters and punctuation. You've probably also used a virtual on-screen keyboard, like those in smartphones and tablets. You might even occasionally use a digital assistant's speech recognition as a form of text entry. And because text-entry is so frequent a task with computers, you probably also have very strong opinions about what kinds of text-entry you prefer: some hate talking to Siri, some love it. Some still stand by their physical Blackberry keyboards, others type lightning fast on their Android phone's virtual on-screen keyboard. And some like big bulky clicky keys, while others are fine with the low travel of most thin modern laptop keyboards.

What underlies these strong opinions? A large set of hidden complexities. Text entry needs to support letters, numbers, and symbols across nearly all of human civilization. How can text entry support the input of the 109,384 distinct symbols from all human languages encoded in [Unicode 6.0|http://www.unicode.org/versions/Unicode6.0.0/]? How can text be entered quickly and error-free, and help users recover from entry errors? How can people _learn_ text entry interfaces, just like they learn handwriting, keyboarding, speech, and other forms of verbal communication. How can people enter text in a way that doesn't cause pain, fatigue, or frustration? Many people with injuries or disabilities (e.g., someone who is fully paralyzed) may find it excruciatingly difficult to enter text. The ever-smaller devices in our pockets and on our wrists only make this harder, reducing the usable surfaces for comfortable text entry.

|typewriter.jpg|A photograph of a Jewett No. 4 typewriter.|A Jewett No. 4 typewriter from 1894.|Unknown|

The history of text entry interfaces predates computers (Silfverberg 2007). For example, typewriters like the Jewett No. 4 shown above had to solve the same problem as modern computer keyboards, but rather than storing the sequence of characters in computer memory, they were stored on a piece of paper with ink. Typewriters like the Jewett No. 4 and their QWERTY keyboard layout emerged during the industrial revolution when the demand for text increased.

Of course, the difference between mechanical text entry and computer text entry is that computers can do so much more to ensure fast, accurate, and comfortable experiences. Researchers have spent several decades exploiting computing to do exactly this. This research generally falls into three categories: techniques that leverage *discrete* input, like the pressing of a physical or virtual key, techniques that leverage *continuous* input, like gestures or speech, and statistical techniques that attempt to *predict* the text someone is typing to _automate_ text entry.

|keyboards.jpg|A photograph of many piles of many computer keyboards.|Standard keyboards|Zinneke CC BY-SA 3.0|

# Discrete input

Discrete text input involves entering a single character or word at a time. We refer to them as discrete because of the lack of ambiguity in input: either a button is pressed and a character or word is generated, or it is not. The most common and familiar forms of discrete text entry are keyboards. Keyboards come in numerous shapes and sizes, both physical and virtual, and these properties shape the speed, accuracy, learnability, and comfort of each.

Keyboards can be as simple as 1-dimensional layouts of characters, navigated with a left, right, and select key. These are common on small devices where physical space is scarce. Multiple versions of the iPod, for example, used 1-dimensional text entry keyboards because of its one dimensional click wheel.

Two-dimensional keyboards like the familiar QWERTY layout are more common. And layout matters. The original QWERTY layout, for example, was designed to minimize mechanical failure, not speed or accuracy. The Dvorak layout was designed for speed, placing the most common letters in the home row and maximizes alternation between hands (Dvorak and Dealey 1936):

|dvorak.png|The Dvorak keyboard layout|The Dvorak keyboard layout.|Tiki katin CC0|

Not all two-dimensional keyboards have a 1-to-1 mapping from key to character. Some keyboards are virtual, with physical keys for moving an on-screen cursor:

|glenayre.jpg|An on-screen keyboard on a pager.|An on-screen keyboard on a pager.|Unknown|

Cell phones in the early 21st century used a *multitap* method in which each key on the 12-key numeric keyboard typically found on pre-smartphone cellphones mapped to three or four numbers or letters. To select the letter you wanted, you would press a key multiple times until the desired letter is displayed. A letter was entered when a new key was struck. If the next letter is on the same key as the previous letter, then the user must wait for a short timeout or hold down the key to commit the desired character. Some researchers sped up multitap techniques like this by using other sensors, such as tilt sensors, making it faster to indicate a character<wigdor03>. Other researchers explored even more efficient forms of text entry with minimal keys, including one with only _4_ keys, where characters are uniquely encoded as sequences of presses of those four keys<mackenzie11>. On particularly small devices like smartwatches, some researchers have explored having the user move the _keyboard_ to select the character they want<shibata16>. Other approaches include portable Bluetooth-connected chording keyboards like the [Twiddler|https://twiddler.tekgear.com/], which can be customized for rapid text entry.

|https://www.youtube.com/embed/mPfktzYsVZI|DriftBoard: A Panning-Based Text Entry Technique for Ultra-Small Touchscreens|DriftBoard: A Panning-Based Text Entry Technique for Ultra-Small Touchscreens|Shibata et al.<shibata16>|

Some keyboards are eyes-free. For example, long used in courtrooms, stenographers who transcribe human speech in shorthand have used chorded keyboards called stenotypes:

|https://www.youtube.com/embed/egLLsM9wN50|STTRs Direct Stenography Demonstation|A video demonstrating how a stenotype works, often used in courtrooms for rapid chorded text entry|Robert Minter|

With 2-4 years of training, some stenographers can reach 225 words per minute. Researchers have adapted these techniques to other encodings, such as braille, to support non-visual text entry for people who are blind or low-vision<azenkot12>:

|https://www.youtube.com/embed/Ot8_lObS1Lc|Perkinput: Eyes-Free Text Entry on Smartphones and Tablets|Perkinput: Eyes-Free Text Entry on Smartphones and Tablets|Azenkot et al.<azenkot12>|

On-screen virtual keyboards like those found in modern smartphones introduce some degree of ambiguity into the notion of a discrete set of keys, because touch input can be ambiguous. Some researchers have leveraged additional sensor data to disambiguate which key is being typed, such as which finger is typically used to type a key<choi15>. Other approaches have studied how users conceptualize touch input, allowing for more accurate target acquisition<holz11>.

|onscreen-keyboard.jpg|A user typing on an iPad on-screen keyboard|On-screen keyboards are now ubiquitous in mobile devices.|Unknown|

# Continuous input

The primary benefit of the discrete input techniques above is that they can achieve relatively fast speeds and low errors because input is reliable: when someone presses a key, they probably meant to. But this is not always true, especially for people with motor impairments that reduce stability of motion. Moreover, there are many people that cannot operate a keyboard comfortably or at all, many contexts in which there simply isn't physical or virtual space for keys, and many people who do not want to learn an entire new encoding for entering text.

Continuous input is an alternative to discrete input, which involves providing a stream of data as input, which the computer then translates into characters or words. This helps avoid some of the limitations above, but often at the expense of speed or accuracy. For example, popular in the late 1990's, the Palm Pilot used a unistroke gesture alphabet for text entry. It did not require a physical keyboard, nor did it require space on screen for a virtual keyboard. Instead, users learned a set of gestures for typing letters, numbers, and punctuation.

|graffiti.png|A diagrm of the Palm Pilot's Graffiti 2 gesture set.|The Palm Pilot's Graffiti 2 gesture set.|Palm, Inc.|

This wasn't particularly fast or error-free, but it was relatively learnable and kept the Palm Pilot small.

Researchers envisioned other improved unistroke alphabets. Most notably, the EdgeWrite system was designed to stabilize the motion of people with motor impairments by defining gestures that traced around the edges and diagonals of a square<wobbrock03>. This way, even if someone had motor tremors that prevented fine motor control, they could still accurately enter text. EdgeWrite has been tested on desktops, mobile devices, joysticks, and even tiny vibrotactile displays like smartwatches<liao16>.

Whereas the unistroke techniques focus on entering one character at a time, others have explored strokes that compose entire words. Most notably, the SHARK technique allowed users to trace across multiple letters in a virtual keyboard layout, spelling entire words in one large stroke<kristensson04>:

|shark.png|An example of a word stroke in the SHARK system, spelling the word system.|An example of a word stroke in the SHARK system, spelling the word system.|Kristensson<kristensson04>|

Researchers have built upon this basic idea, allowing users to use two hands instead of one for tablets<bi12>, allowing unused parts of the gesture space for creative expression<alvina16>, and optimizing the layout of keyboards using Fitts' law for speed<rick10>.

As interfaces move increasingly away from desktops, laptops, and even devices, researchers have investigated forms of text-entry that involve no direct interaction with a device at all. This includes techniques for tracking the position and movement of fingers in space for text entry<yi15>:

|https://www.youtube.com/embed/gYkSOzKY1LQ|ATK: Enabling Ten-Finger Freehand Typing in Air Based on 3D Hand Tracking Data|ATK: Enabling Ten-Finger Freehand Typing in Air Based on 3D Hand Tracking Data|Yi et al.<yi15>|

Other techniques leveraging spatial memory of keyboard layout for accurate text input on devices with no screens<chen14> and eyes-free entry of numbers<azenkot13>.

Handwriting and speech recognition have also long been a goal in research and industry. While both continue to improve, and speech recognition in particular becomes ubiquitous, both continue to be plagued by recognition errors. People are finding many settings in which these errors are tolerable (or even fun!), but they have yet to reach levels of accuracy to be universal, preferred methods for text entry.

# Predictive input

The third major approach to text entry has been predictive input, in which a system simply guesses what a user wants to type based on some initial information. This technique has been used in both discrete and continuous input, and is relatively ubiquitous. For example, before smartphones and their virtual keyboards, most cellphones offered a scheme called T9, which would use a dictionary and word frequencies to predict the most likely word you were trying to type.

These techniques leverage Zipf's law, an empirical observation that the most frequent words in human language are exponentially more frequent than the less frequent words. The most frequent word in English ("the") accounts for about 7% of all words in a document, and the second most frequent word ("of") is about 3.5% of words. Most words rarely occur, forming a long tail of low frequencies.

This law is valuable because it allows techniques like T9 to make predictions about word likelihood. Researchers have exploited it, for example, to increase the relevance of autocomplete predictions<mackenzie01>, and even to recommend entire phrases rather than just words<arnold16>. These techniques are widely used in speech and handwriting recognition to increase accuracy, and are now ubiquitous in smartphone keyboards.

# The past, present, and future of text entry

Our brief tour through the history of text entry reveals a few important trends:

* There are _many_ ways to enter text into computers and they all have speed-accuracy tradeoffs. 
* The vast majority of techniques focus on speed and accuracy, and not on the other experiential factors in text entry, such as comfort or accessibility. 
* There are many text entry methods that are inefficient, and yet ubiquitious (e.g., QWERTY); adoption therefore isn't purely a function of speed and accuracy, but many other factors in society and history. 

As the world continues to age, and computing moves into every context of our lives, text entry will have to adapt to these shifting contexts and abilities. For example, we will have to figure out how to efficiently enter text in augmented and virtual realities, which may require require more sophisticated and efficient ways of correcting errors in speech recognition. Therefore, while text entry may _seem_ like a well-explored area of user interfaces, every new interface we invent demands new forms of text input.