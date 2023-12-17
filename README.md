# How-to-design-a-hard-fault-FSAE-
![WhatsApp Image 2023-12-15 at 11 56 50 PM](https://github.com/Anoushka6/How-to-design-a-hard-fault-FSAE-/assets/139247452/3e59fc5c-5066-428b-aeef-ed0bcca890c8)

Hello and welcome! Join us on a journey into the realm of innovation as we explore the development of the hard-fault circuit for our exceptional 2024 Formula Student car, Genesis. After securing an impressive 7th place overall at the highly competitive Formula Bharat 2023 in India, our story highlights the seamless integration of advanced technology and automotive expertise. Below, we share insights into the process that led us to the design of our hardfault circuit, highlighting the dedication, expertise, and teamwork that fueled our journey to excellence. 


Supplies:
 
  Free Softwares to start your journey in PCB design and circuit simulations 
 
   https://www.kicad.org/download/
  
   https://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html

 What Is the Hardfault? What Is Its Significance?
 
"Hardfault” is a term used in Formula Student and Formula SAE (Society of Automotive Engineers) contests. It represents an exception that occurs when an error happens during normal or exception processing. Other exception mechanisms cannot handle all types of faults. Hard faults are usually used for unrecoverable system failures. It's essential to ensure the overall operation of the Formula Student vehicle safely and successfully, both in practice and during competition. This circuit serves as a vital safety component. The vehicle’s shutdown circuit includes the hardfault circuit, a non-programmable circuit that shuts down the entire car. 

Implementation

We want to express our sincere gratitude to JLCPCB for their generous sponsorship! Initially, we handcrafted all our boards, but as the complexity and number of components in each circuit grew, it became nearly impossible to continue that way. The support from JLCPCB has been significant in the success and journey of our Genesis 2024 Formula Student car.

![FO1IM7NLQ6N339C](https://github.com/Anoushka6/How-to-design-a-hard-fault-FSAE-/assets/139247452/c09f1d91-2621-4f34-a542-3ea773eff2b7)

Your contribution has been instrumental in helping us achieve our goals and showcase our innovation on the track. We deeply value our partnership and eagerly anticipate the continuation of our collaboration in the future. 
We wholeheartedly recommend JLCPCB because they are simply the best in the business. If you're aiming for the highest quality PCBs, check out this link: https://jlcpcb.com/HAR

Design Flow and Schematic

Latches, which are digital circuits designed to retain a single bit of information until prompted by fresh input signals, form the fundamental principles on which the hardfault circuit operates. These latches serve as transient storage elements in digital systems, preserving binary data

![1 (2)](https://github.com/Anoushka6/How-to-design-a-hard-fault-FSAE-/assets/139247452/bd2950ff-3262-4622-8e19-456f6272c212)

Within this context, the CD4044 IC plays a crucial  role, housing four R-S latches crafted with NAND logical gates. A shared 3-state ENABLE input governs all four latches, with a logic “1” linking latch states to the Q outputs and a logic “0” disconnecting them, resulting in an open circuit condition on the Q output. This 3-state feature facilitates the common busing of outputs, and the IC boasts features such as high noise immunity, ESD protection, and effective thermal overload safeguards.

![2 (2)](https://github.com/Anoushka6/How-to-design-a-hard-fault-FSAE-/assets/139247452/37407cb5-e7f5-4e75-a003-16fc2ac16b2b)


Thus far, we've delved into the process of reading the sensor and verifying whether specific conditions are met or not. The outputs from the R-S latch are then directed to the IC 7425 NOR gate. This NOR gate is particularly significant due to its capability to execute logical NOR functions, enhancing the overall functionality and reliability of the system. To offer manual control, a reset button is integrated, manually linked to the IC 4044, providing an additional layer of versatility to the system. 

Design PCB Layout and Gerber

![5 (2)](https://github.com/Anoushka6/How-to-design-a-hard-fault-FSAE-/assets/139247452/6f882a45-7445-4b7d-9fd7-22847b65e20d)

After we designed our schematic, we then designed the PCB layout, followed by generating our Gerber files. 
After finalising all of our designs, we sent them to JLC PCB for manufacturing. We assembled the boards, and the hardfault worked well every time we needed it.
 Thanks to our sponsor, JLCPCB, for giving us the opportunity, and remember, here is your link: https://jlcpcb.com/HAR

Steps to Order JLC PCB

Now that the PCB design is complete, it's time to place an order for the PCBs. To do this, simply visit JLCPCB's website and click on the "QUOTE NOW" button. It's worth mentioning that JLCPCB is one of the sponsors of this project. Shenzhen JLC Electronics Co., Ltd., the parent company, stands as the largest PCB prototype enterprise in China and is a high-tech manufacturer specializing in rapid PCB prototypes and small-batch PCB production.
At JLCPCB, you have the flexibility to order a minimum of 5 PCBs for just $2. To initiate the manufacturing process, upload the Gerber file that you downloaded in the previous step. You can either upload the ZIP file or use the drag-and-drop feature for the Gerber files. Once the ZIP file is successfully uploaded, you'll receive a confirmation message at the bottom of the page.

For assurance, you can review the PCB in the Gerber viewer to ensure everything is in order. After confirming, you can proceed with placing your order.
For a more visual guide, you can watch a tutorial video on the process: [JLCPCB Tutorial Video] (https://www.youtube.com/watch?v=ZZWdaWAr5A8 ).

If you've reached this point, we extend our sincere thanks for reading the entire article.

Best regards,

Team CFR…
