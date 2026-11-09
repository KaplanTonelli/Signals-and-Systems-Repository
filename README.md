# Signals and Systems


## 1. System purpose

- **Problem and real-world context:** I cant tell how much time something has left
- **Intended user:** People who want to know the time of something from far away
- **What information should your signals communicate?** getting close to being done, times up, and still lots of time left
- **How does the user interpret and use that information?** If its yellow is 49% or less, green is 50% or more, and red is 0%

## 2. State table and pattern plan


| Step | State/message name | LED Color | LED Color | LED Color | Duration (ms) | Meaning to the user |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Over 50% | green | green | green | 15 secs | timers over halfway |
| 2 | under 50% | yellow | yellow | yellow | 15 secs | timers halfway |
| 3 | 0% | red | red | red | forever | timers up |

**Sequence:** Green → yellow → red → repeat  

## 3. Circuit design


![Circuit diagram screenshot](circuit.png)

### Ohm's law calculations


| LED | Arduino output voltage (V) | LED voltage drop (V) | Calculated resistor voltage (V) | Target current (A) | Calculated resistance (Ω) | Chosen resistance (Ω) | Estimated actual current (A) |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Green LED | 5.0 | 3V | 2V | 15mA | 133Ω | 230Ω | 8mA |
| Yellow LED | 5.0 | 2V | 3V | 15mA | 200Ω | 230Ω | 13mA |
| Red LED | 5.0 | 2V | 3V | 10mA | 300Ω | 330Ω | 9mA |

## 4. Testing and revision


**Person 1:** Person 1Said that it was a timer but it took a little bit for them to understand, he said that I should make it more visually appealing.

**Person 2:** Person 2 couldn't tell what it was but realized after I told them, they said I should make the timer faster because it takes too long

**Did their interpretations match your intended meaning? Explain:** Yes, mostly

**Revisions made to the system based on feedback**
Based on person 2's feedback I made it faster so its easier to understand

**Revision and reason**: Timer is faster

**Result after testing the revision:** It now is a faster timer

## 5. Video Demonstration

[Video demonstration](https://www.youtube.com/watch?v=E91wwh8d3MU&feature=youtu.be)