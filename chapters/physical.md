Whereas the three-dimensional output we discussed in [the previous chapter|3D] can create entirely new virtual worlds, or enhanced versions of our own world, it's equally important that software be able to interface with the physical world. One of the first research papers to recognize this was the seminal work _Tangible Bits: Towards Seamless Interfaces between People, Bits and Atoms_<ishii97>. In it, Ishii and Ullmer described a rift between the digital and physical world:

"
We live between two realms: our physical environment and cyberspace. Despite our dual citizenship, the absence of seamless couplings between these parallel existences leaves a great divide between the worlds of bits and atoms. At the present, we are torn between these parallel but disjoint spaces... Streams of bits leak out of cyberspace through a myriad of rectangular screens into the physical world as photon beams. However, the interactions between people and cyberspace are now largely confined to traditional GUI (Graphical User Interface)-based boxes sitting on desktops or laptops. The interactions with these GUIs are separated from the ordinary physical environment within which we live and interact. Although we have developed various skills and work practices for processing information through haptic interactions with physical objects (e.g., scribbling messages on Post-It notes and spatially manipulating them on a wall) as well as peripheral senses (e.g., being aware of a change in weather through ambient light), most of these practices are neglected in current HCI design because of the lack of diversity of input/output media, and too much bias towards graphical output at the expense of input from the real world. " Ishii and Ullmer<ishii97>

This basic idea, that the massive rift between our physical and digital worlds should be bridged by a diversity of new physical input and output media, dovetailed Weiser's vision of ubiquitous computing<weiser91>. However, rather than envisioning a world of embedded computing, it focused on our embodied experiences with physical objects. Both of these themes are another example of how interfaces play a central role in [mediating our interactions|mediation].

The impact of this vision was an explosion of research to create more physical input and output. In this chapter, we'll discuss this research, and the history of physical computing that it build upon. 

# Printing

Most people who've interacted with computers have used a printer at some point in their life to turn bits into atoms. The basic principle is simple: take a digital document and create a facsimile with paper and some kind of mark, such as spraying ink (inkjets), burning the paper (laser printers), or one of a variety of other approaches. 

Why was printing so important as computers first became ubiquitous?
For most of the 20th century, paper was the central medium for transmitting information. We used typewriters to create documents. We stored documents in file cabinets. We used photocopiers to duplicate documents. The very notion of a file and folder in graphical user interfaces mirrored the ubiquity of interacting with paper. Printers were a necessary interface between the nascent digital world and the dominant paper-based world of information. 

One of the earliest forms of digital printing was the stock ticker machine, which printed text on a thin strip of paper on which messages are recorded:


|tickertape.jpg|Two women reading ticker tape at the New York Stock Exchange.|Two women at the Waldorf-Astoria Hotel in 1918 operating the ticker machines and stock exchange boards|U.S. War Department.

While ticker tape was the most ubiquitous before the advent of digital computers, printing devices had long been in the imagination of early computer scientists. [Charles Babbage|https://de.wikipedia.org/wiki/Charles_Babbage] was an English mathematician and philosopher who first imagined the concept of a programmable digital computer in 1822. He also imagined, however, a mechanical printing device that could print the results of his imagined differencing machine. Eventually, people began to engineer these printing devices. For example, consider the dot matrix printer shown in the video below, which printed a grid of ink. These printers were ubiquitous in the 1980's, and a general extension of both ticker tape printers and a deeper integration with digital printing from general purpose computers. This was the beginning of a much greater diversity of printing mediums we use today, which use toner, liquid ink, solid ink, or dye-sublimation--. 

|https://www.youtube.com/embed/u8I6qt_Z0Cg|A dot matrix printer|Dot matrix printers can also be used to play inspiring montage music.|Midi Desaster|

Most of these printing technologies have focused on 2-dimensional output because the documents we create on computers are primarily 2-dimensional. However, as the plastics industry evolved, and plastic extruders reshaped manufacturing, interest in democratizing access to 3D fabrication expanded. This led to the first 3D printer, described in a U.S. patent in 1984, which described a process for generating 3D objects by creating cross-sectional patterns of an object<hull84>. These early visions for personal 3D printing, combined with decades of research on the basic technologies required to manufacture printers at scale, eventually led to a new market for 3D printing, including companies like [MakerBot|https://www.makerbot.com/]. These printers also required the creation of new software to model printable 3D forms. 

While the basic idea of 3D printing is now well established, and the market for 3D printers is expanding, researchers have gone well beyond the original premise. Much of this exploration has been in exploring materials other than plastic. One example of this is an approach to printing _interactive electromechanical objects with wound in place coils_<peng16>. These objects, made of copper wire, and structural plastic elements, allows for the printing of objects like actuated arms of toys, electric motors, and electronic displays:

|https://www.youtube.com/embed/5MEYe-z9GKo|A 3D Printer for Interactive Electromagnetic Devices|Printing electromagnetic objects.|Peng et al.<peng16>|

Another project explored printing with wool and wool blend yarn to create soft felt objects rather than just rigid plastic objects<hudson14>. Techniques like this and the one above simultaneously innovate in printing techniques, but also in exploring the possibilities of new media for bridging the digital and physical world. 

|https://www.youtube.com/embed/YhXIWyfI7Cw|Printing Teddy Bears: A Technique for 3D Printing of Soft Interactive Objects|Printing with felt.|Scott Hudson<hudson14>|

These new forms of printing pose new challenges in authoring. One cannot print arbitrary 3D shapes with 3D printers, and so this requires authors to understand the limitations of printing methods. This lack of understanding can lead to failed prints, which can be frustrating and expensive. Some researchers have explored "patching" 3D objects, calculating additional parts that must be printed and mounted onto an existing failed print to create the desired shape<teibrich15>. Other research has investigated new software tools for extending, repairing, or modifying everyday objects by modeling those objects and streamlining the creation of attachment objects<chen15>:

|https://www.youtube.com/embed/obui6I2dzxk|Encore: 3D Printed Augmentation of Everyday Objects with Printed-Over, Affixed and Interlocked Attachments|Designing and printing attachment objects|Xiang Chen<chen15>|

These techniques, while not advancing _how_ objects are printed, innovate in how we author objects to print, much like research innovations in word processing software from the 1980's and 1990's. 

# Morphing

Whereas printing is all about creating physical form to digital things, another critical bridge between the physical and digital world is adapting digital things to our physical world. Screens, for example, are one of the key ways that we present digital things, but their rigidity has a way of defining the physical form of objects, rather than objects defining the physical form of screens. The iPhone is a flat sheet of glass, defined by the screen; a laptop is shape of a screen. Researchers have long pondered why are screens have to be flat, and have envisioned different forms of output that might have new unimagined benefits. 

Some research has focused on making screens flexible and bendable. For example, one technique takes paper, plastics, and fabrics, and makes it easy to create programmable shape-changing behaviors with those materials<ou16>. As seen in the video below, this creates a new kind of digital display that can dynamically convey information and shape. 

|https://www.youtube.com/embed/b1vrvDUr1Ds|aeroMorph - Heat-sealing Inflatable Shape-change Materials for Interaction Design|Programmable, shape-changing materials| Ou et al.<ou16>|

Other projects have created _stretchable_ user interfaces with sensing capabilities and visual output, allowing for conventional experiences in unconventional places<wessely16>. As seen in the video below, these screens adapt to objects' physical forms, rather than requiring objects to adapt to a rectangular display:

|https://www.youtube.com/embed/gPVdvxfeE50|Stretchis: Fabricating Highly Stretchable User Interfaces|Stretchable interfaces|Wessely et al.<wessely16>|

Some research has even explored foldable interactive objects by using thin-film printed electronics<olberding15>. The video below shows several examples of the types of new interactive physical forms that such materials might enable:

|https://www.youtube.com/embed/yQjhe0Ravf0|Foldio: Digital Fabrication of Interactive and Shape-­Changing Objects With Foldable Printed Electronics|Foldable interfaces.|Olberding et al.<olberding15>|

This line of research innovates in both the industrial forms that interfaces take, while offering new possibilities for how they are manipulated physically. It envisions a world in which digital information might be presented and interacted with in the shape most suitable to the data, rather than adapting the data to the shape of a screen. Most of these innovation efforts are not driven by problems with existing interfaces, but opportunities for new experiences that we have not yet envisioned. With many innovations from research such as foldable displays now make it to market, we can see how technology-driven innovation, versus problem-driven innovation, can struggle to demonstrate value in the marketplace. 

# Haptics

Whereas morphing interfaces change the _structural_ properties of the interface forms, others have focused on offering physical, tangible feedback. Feedback is also critical to achieving the vision of tangible bits, as the more physical our devices become, the more they need to communicate back to us through physical rather than visual form. We call physical feedback *haptic* feedback, because it leverages people's perception of touch and sense of where their body is in space (known as proprioception). 

Haptic feedback varies in its goals. For instance, some haptic feedback operates at a low level of human performance, such as this idea, which recreates the physical sensation of writing on paper with a pencil, ballpoint pen or marker pen, but with a stylus<cho16>:

|https://www.youtube.com/embed/RNn0_rkFXkw|RealPen: Providing Realism in Handwriting Tasks on Touch Surfaces using Auditory-Tactile Feedback|Simulated writing feedback.|Cho et al.<cho16>|

Other haptic feedback aims to provide feedback about user interface behavior using physical force. For example, one project used electrical muscle stimulation to steer the user's wrist while plotting charts, filling in forms, and other tasks, to prevent errors<lopes15>. Another used airflow to provide feedback without contact<lee16>:

|https://www.youtube.com/embed/QdSK_K3Spcw|Designing a Non-contact Wearable Tactile Display Using Airflows|Feedback with airflow.|Lee and Lee<lee16>|

Many projects have used haptics to communicate detailed shape information, helping to bring tactile information to visual virtual worlds. Some have used ultrasound to project specific points of feedback onto hands in midair<carter13>. Others used electrovibration, integrated with touch input, enabling the design interfaces that allow users to feel virtual elements<bau10>. Some projects have used physical forms to provide shape information, such as this gel-based surface imposed on a multi-touch sensor allowing for freely morphed arbitrary shapes<miruchna15>:

|https://www.youtube.com/embed/o8W6qbwPhwU|GelTouch: Localized Tactile Feedback Through Thin, Programmable Gel|Gel-based multi-touch tactile feedback.|Miruchna et al.<miruchna15>|

Some work leverages *visuo-haptic illusions* to successfully trick a user's mind into feeling something virtual. For example, one work displayed a high resolution visual form with tactile feedback from a low-resolution grid of actuated pins that move up and down, giving a sense of high-resolution tactile feedback<abtahi18>. Some projects have created a sense of virtual motion by varying waves of actuator motion left or right<kaye12>. In anticipation of virtual reality simulations of combat, some have even created perceptions of being physically hit by tapping the skin gently while thrusting a user's arm backwards using electrical muscle stimulation<lopes15>:

|https://www.youtube.com/embed/CNEZguz1NEU|Impacto: Simulating Physical Impact by Combining Tactile Stimulation with Electrical Muscle Stimulation|Simulating impact.|Lopes et al.<lopes15>|

All of these approaches to haptic feedback bridge the digital and physical worlds by letting information from digital world to reach our tactile senses. In a sense, all haptic feedback is about bridging gulfs of evaluation in physical computing: in a physical device, how can the device communicate that it's received input and clearly convey its response?

---

While this exploration of media for bridging bits and atoms has been quite broad, it is not yet deep. Many of these techniques are only just barely feasible, and we still know little about what we might do with these techniques, how useful or valued these applications might be, or what it would take to manufacture and maintain the hardware they require. Nevertheless, it's clear that the tangible bits that Ishii and Ullmer envisioned are not only possible, but rich, under-explored, and potentially transformative. As the marketplace begins to build some of these innovations into products, we will begin to see just how valuable these innovations are in practice. 