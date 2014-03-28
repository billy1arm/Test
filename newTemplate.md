SMSG_WEATHER
-----
[Home](/README.md) &middot; [Packets](index.md)

Data QA Check: 
   ![Unchecked](/images/unkZero.gif)
   ![Unchecked](/images/unkOne.gif)
   ![Unchecked](/images/unkTwo.gif)
   ![Unchecked](/images/unkThree.gif)
   ![Unchecked](/images/unkFour.gif)

###Usage 

  Sent whenever the weather is updated.

###Structure

Name                          | Type                  | Description
----------------------------- | --------------------- | -----------
Weather Type                  | uint32                | See below.
Density                       | float                 | density must be between 0.3 and 2.0
Sound Type                    | uint32                | See below.
dummy                         | uint8                 | 0 - Empty Byte

####Additional Information 


Weather Type                  | Value                  
----------------------------- | ---------------------  
Normal (Sunny)                | 0                      
Fog                           | 1
Rain                          | 2                     
Heavy Rain                    | 4                     
Snow                          | 8                     
Sandstorm                     | 16                     

  
Sound Type                    | Value                 
----------------------------- | --------------------- 
No Sound                      | 0                     
Light Rain                    | 8533
Medium Rain                   | 8534                  
Heavy Rain                    | 8535                  
Light Snow                    | 8536                  
Medium Snow                   | 8537
Heavy Snow                    | 8538
Light Sandstorm               | 8556                   
Medium Sandstorm              | 8557                   
Heavy Sandstorm               | 8558                   


####Example Packet

    SMSG_WEATHER Length: ??
    |-------------------------------------------------|---------------------------------|
    | 00 01 02 03 04 05 06 07 08 09 0A 0B 0C 0D 0E 0F | 0 1 2 3 4 5 6 7 8 9 A B C D E F |
    |-------------------------------------------------|---------------------------------|
    | ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ??             | . . . . . . . . . . . .         |
    |-------------------------------------------------|---------------------------------|

####Opcode Value

Client | Build | Value  | Notes
------ | ------|--------|------  
1.12.1 | 5875  | 0x2F4  | This offset remained the same until the Cataclysm Client
 4.3.4 | 15595 | 0x2904 |
 5.3.0 | 17128 | 0x1391 |

QA Key: 
   Confirmed ![Confirmed](/images/KeyOk.gif)
   Unchecked ![Unchecked](/images/keyUnk.gif)
   Incorrect ![Incorrect](/images/keyFail.gif)


-----
Proudly brought to you by:
<br>
[![getMaNGOS](https://www.getmangos.eu/!assets_mangos/logo.png)](http://getmangos.eu)
