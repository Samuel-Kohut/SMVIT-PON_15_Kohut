# SMVIT-PON\_15\_Kohut



Project Repository for the university subject SMVIT.

---

## About Me

Hi, my name is **Samuel Kohút**, and I’m currently finishing my Master’s degree in **Intelligent Software Systems (ISS)** at the Faculty of Informatics and Information Technologies, Slovak University of Technology in Bratislava. I already hold a Bachelor’s degree in Computer Science and am now in my final 5th year of studies.



💻 **Background \& Experience**



* I’ve worked on various academic and personal projects, ranging from data structures, web applications and games to AI-driven solutions such as **face recognition** and **reinforcement learning in Atari games** (my diploma thesis).
* Professionally, I’ve gained over 2.5 years of experience as a **Backend Developer in Java**, where I focused on building web applications. Before that, I worked two years in the logistics sector at Metro supermarket.
* My technical strengths lie in **coding**, problem-solving, and building practical software systems.



🎹 **Current Project**  


For my Systems Thinking course, I’m working on a **LED Piano Trainer**. This project uses a Raspberry Pi Pico and LEDs to gamify the learning process for piano beginners. Instead of traditional sheet music, LEDs light up to guide which keys to press, making learning feel more like playing a game.



🚀 **Interests \& Goals**



* I enjoy **backend programming, web development, and creating projects that solve real problems**.
* While I’ve done a lot of work in AI, it’s not where I see my long-term future — I prefer coding, building systems, and exploring **gamification concepts** that make learning fun.
* Long term, I see myself growing as a **skilled developer**, either working on impactful projects or creating something of my own.



🎯 **Fun Facts**



* Born in **Snina, Slovakia**, a small city in the east.
* In my free time, I enjoy **rock climbing, gaming, watching YouTube, anime, and reading manga**.
* I love music, even though I’ve never played an instrument myself — this makes the LED piano project even more exciting for me, as I hope to share it with my younger family members.

---

## <STHDF-LEDPIANO> Project Summary

**Project ID:** STHDF-LEDPIANO  
**Project Name:** Light-Up Keyboard Learning Aid  
**Product Name:** LED Piano Trainer  

### Team Members
- **Samuel Kohút** – system designer, hardware & firmware developer, documentation

Role: end-to-end responsibility for concept, implementation, testing and documentation.


### Purpose
Build a **physical learning aid for piano beginners** that uses a 3D-printed LED bar above the keys to guide which key to press. Practising should feel more like a **rhythm game** than reading sheet music, and the project should connect my software skills with real hardware and makerspace tools.


### Individual Visions
- Create something useful for my **younger cousin** to make learning piano more fun.  
- Combine **embedded programming (Raspberry Pi Pico), 3D printing and system thinking** in one coherent project.  
- Leave behind a **reproducible, well-documented build** that others can recreate or extend.


### Team Vision
Even as a one-person project, the vision is to:
- Have a **fully working demo setup** (MIDI keyboard + LED bar + controller box).  
- Maintain clear **documentation and knowledge contributions** (GitHub + OneNote).  
- Provide a **short demo video and final presentation** that show real learning value, not just blinking LEDs.


### Team Mission
- Design and print a **modular LED extension** that sits on top of the keys and lights exactly one cell per key.  
- Implement firmware on the Raspberry Pi Pico to drive the WS2812B LED strip based on song data.  
- Experiment with a PC pipeline (YouTube → audio → MIDI → notes → LEDs).  
- Evaluate how well the system supports learning and what would be needed to turn it into a “real” product.


### Strategy
- Use a **simple, safe hardware design**: no modification of the keyboard
- Use **WS2812B addressable LEDs** for simple wiring and per-key colour control.  
- Keep Pico firmware small and move heavy work (MIDI, transcription, song processing) to the **laptop**.  
- Iterate in small steps: blink tests → key mapping → simple melodies → practice features.  
- Document all major steps with text and photos in **OneNote** and **GitHub**.


### End Customer
- **Primary:** complete piano beginners (children, students) who prefer a visual, playful approach.  
- **Secondary:** parents and music teachers looking for a motivational practice tool.


### Expected Effort
- Hardware design, 3D printing, wiring: **15–25 hours**  
- Firmware (MicroPython on Pico), mapping, melodies: **10–20 hours**  
- Documentation, knowledge contributions, demo, presentation: **25–35 hours**   


### Goals and Expectations
- Working prototype for **two octaves** on the AKAI LPK25, with one LED per key box.  
- At least **2–3 songs from youtube piano covers** playable as LED sequences.  
- A **complete GitHub repo** with wiring diagrams, 3D models, setup instructions and sample code.  
- A short **demo video** used in the final presentation.  
- Reflection on how the project illustrates **systems thinking** (hardware, software, user, documentation, ecosystem).

### Solution Description

**Hardware**
- AKAI LPK25 MIDI keyboard (25 keys, two octaves).  
- WS2812B addressable LED strip routed through a **3D-printed light bar** (one light box per key).  
- Raspberry Pi Pico WH as controller.  
- Breadboard, jumpers, resistors and a **3D-printed electronics box** to hide wiring and power.

**Firmware**
- MicroPython code using a PIO-based Neopixel driver.  
- Mapping from key index / MIDI note to LED index.  
- Song player to light notes in sequence with tempo control, with room for chord support later.

**PC Pipeline (planned)**
- Convert piano covers (e.g. YouTube) to MIDI.  
- Clean and adapt songs to the LPK25 note range.  
- Send note events over USB serial to the Pico using a simple text protocol.

### Project Roadmap

#### Phase 1 – Planning & Research (DONE)
- Defined goal, scope and target users.  
- Analysed LED placement options: rejected internal LEDs, chose external light bar.

#### Phase 2 – Infrastructure (DONE)
- Set up Raspberry Pi Pico with MicroPython.  
- Verified LED strip control and created setup tutorials as knowledge contributions.

#### Phase 3 – Hardware Assembly & 3D Printing (DONE / REFINING)
- Printed test pieces with different wall thicknesses for optimal light diffusion.  
- Printed two-octave LED bar plus an extra box for the last key.  
- Bent and routed LED strip to fit one LED per box.  
- Printed enclosure box for Pico and cabling.

#### Phase 4 – Firmware & Interaction (IN PROGRESS)
- Finalize key → LED mapping.  
- Implement simple melody playback and tempo control.

#### Phase 5 – Integration & Evaluation (PLANNED)
- Prototype PC pipeline for sending note events.  
- Test with real users and gather feedback.

#### Phase 6 – Finalization (PLANNED)
- Polish code and documentation.  
- Record demo video and prepare final presentation.


### Reached Results
- Working hardware platform: Raspberry Pi Pico + WS2812B strip + power + MIDI keyboard.  
- Fully functional **3D-printed LED extension bar** and electronics box mounted on the keyboard.  
- LEDs can light up per key box with good diffusion and alignment.  
- GitHub and OneNote already contain initial documentation, photos and setup tutorials.


### Experiences
- Learned that real products require **mechanical compromises** (e.g. giving up on internal LEDs after inspecting the keyboard).  
- Saw how makerspace tools (3D printing, physical experiments) are essential for iterating on design.  
- Better understood the need to plan the **whole system** – wiring, mechanics, code, user interaction and documentation.


### Positive Experiences
- Seeing the first fully lit LED bar on top of the keys was a huge motivation boost. The project finally felt real.  
- It like that this can actually help my family, not just pass a course.  
- Nice fit between **course ecosystem** (GitHub, OneNote, KNIFES) and how I naturally like to work as a developer.


### Potential for Improvements
- Add a **practice mode** where LEDs wait until the correct key is pressed, with colours for correct/incorrect notes.  
- Add a simple **configuration UI** to pick songs and tempo.  
- Improve portability so the LED bar + box can be adapted to other 25-key or 37-key keyboards.  
- Turn the project into a **documented open-source kit** for other students, teachers or makerspaces.


---
