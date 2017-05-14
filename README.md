# ArduRay
## A New ArduPilot Frame Description for an AUV: Melds ArduPlane and ArduSub. For BeagleBone Blue


Hey All,

So the story goes that I've been trying to bring to life a particular AUV (autonomous underwater vehicle) for a long time. Feels like forever coming, but it looks like the time is finally right when I can actually make it happen.

The AUV I'm working on is a tremendously fun project. For me it embodies my lifelong love of ocean exploration, and brings my professional skills in optics and mechanical engineering to ocean robotics. From lengthy discussions with other engineers, the project touches on so many areas of technical interest that it clearly excites a whole spectrum of talent. Even to non-technical folks though, the "OneFish" seems to have a charm that captures the imagination.

The good news is that I have decades of experience in precision mechanical design, with a specialty for optical devices. I also now have a personal CNC machine shop that can be programmed straight from my CAD workstation. The other critical piece of the puzzle is provided by the Open Source community, whose combined efforts have brought the software/firmware/hardware into a realm that, with some help, I can muscle through.

The bad news is I'm at the foot of the Linux/Github learning curve. I was steeped in the DOS world (starting in 1989), and dabbled with a few programming languages (including C, and a pretty good mastery of LISP). I've had some Windows coding exposure, and have collaborated on many embedded device developments. Despite that primer, this stuff is not coming easily. It exposes my present weaknesses in understanding of networks and low-level coding. Well OK then: I'm going at the textbooks now like a dog with a bone in his teeth, -a BeagleBone Blue as it happens- so please bear with me as I come up to conversational highway speed.

Conceived in 2001, the project proposal decsribed an AUV originally intended to operate 24/7 for missions of up to a couple of months in the ocean (i.e., until bio-fouling becomes an issue). I unsuccessfully pitched a much more ambitious project back then, including the development of an expensive IMU/controller, an optical sensor module with custom lenses, and a complete GCS. That proposed OneFish would carry the necessary photovoltaic collection area on its wings to recharge at mid-day in a few hours. During its basking time, uploads and downloads were possible. A satellite in the sea for oceanography. As an in situ data collection platform, OneFish could deliver itself across thousands of miles of open ocean. As it turned out, OneFish was too expensive and complex an undertaking for its day. After literally thousands of hours of development, OneFish never saw the light of day.

With the upwelling of the Open Source community, and with technical advances in portable devices and robotics hardware, the context of such a proposal has changed. This current project is the second major variant: the scaled-down, tabletop-size "OneFish2". Following a 3D CAD mechanical feasibility study, and breadboarding a system using the BeagleBone Blue, I think an interesting variant of the project is now affordably possible as an "all-day" device.

Think of it as a kind of "SnorkelFish". It's appearance, like the original OneFish, is similar to a stingray, which happens here as an evolutionary necessity. Its need for a large solar surface area for energy collection, and a low frontal area (for hydrodynamic efficiency), seems to beg biomimicry of a ray. The OneFish2 "snorkel" variant spends most of its time on the surface within 50 km of shore, driveable with real-time FPV, taking short autonomous dives to depths of up to 50 meters. Imagine unobtrusively tagging along with a pod of whales or schools of fish, or hanging out with sea turtles, dolphin and otters, or just exploring a reef. Deeper diving and longer range models will inevitably follow.

My AUV Project Repository will be called ArduRay. The "Frame" is functionally equivalent to a twin-engine "Flying Wing" with elevons, where differential motor thrust controls yaw. Essentially, "ArduRay" is the ArduPlane flying wing firmware combined with ArduSub firmware, and the mashed code parsimoniously tweezed and compiled for the BeagleBone Blue. ROS will be integrated in a later phase, as will a number of optical and acoustic devices. At this stage, i.e., the very beginning, Mission Planner is the only GCS I've worked with, but going forward I'll compare the arguments for other GCS packages.

The OneFish architecture describes a vessel with a slight positive bouyancy. In the event of unplanned battery exhaustion while underway, the vessel will float to/upon the surface to recharge and drive "home" for recovery.

Its wing profile is inverted to provide negative lift as it travels forward. The wings contain thin centrifugal pump impellers that are ducted to draw water from the leading edge and exhaust through the thrust-vectoring elevons. This thin centrifugal pump architecture has been modeled in CAD, and flow simulations performed, verifying feasibility. I'll be optimizing and prototyping the pump sub-system in the coming weeks.

OneFish2 will function as an FPV immersive camership. Personally, the OneFish platform is an opportunity to bring my optomechanical experience and my interest in AI to ocean exploration. This initial launch will carry a simple optical system. When surfaced, the OneFish2 hull tilts vertical, pendulous, while the wing follows the water surface. In this mode the operator has 360° view from two cameras: one above and one below the surface. The two immersive experiences will aid real-time navigation and unique perspective on a marine environment. 

The OneFish architecture is very scalable, and there are several obvious product niche possibilities. From kid's toys to sophisticated hobby-grade, all the way to sensor-rich, research-grade AUV's. Swarms could be exercised for long-term search and recovery, or high-resolution mapping. Maybe a variant that serves as a scuba buddy for driveable towing, nearshore communications, and follow-me video. Larger OneFish (about 4X the size of OneFish2) will achieve proportions where a balanced, 24/7 energy budget is possible from a few hours of midday sun. As its software becomes more sophisticated, OneFish will become increasingly autonomous. As a mobile, 24/7 robot operating in a vast and dynamic organic environment, OneFish is a perfect platform to push the limits of AI and machine learning.

I do hope this project will capture the imaginations of more skilled developers. I'm dusting-off my ancient coding skills, and learning to use the new tools, languages and structures. At the moment the BeagleBone Blue and other electronics hardware are mounted to a breadboard, running Mirkix ardupilot-copter-blue. I'll begin physical prototyping of the actual "hull" and wing hardware on my CNC once the breadboard is functional with the proposed ArduRay (Arduplane-ArduSub-Blue) build.

For me, the mechanical hardware is the easy part, as I design and build several new mechanical products each year. I could make parts available to others, given expressed interest. Nowadays a lot of iterative guesswork is eliminated with virtual prototyping and by using multi-physics CAD simulations: prototypes are typically highly functional. SolidWorks is my CAD platform of choice. So far I've invested a few hundred hours into the WIP OneFish2 architecture. Experience tells me that those few hundred hours have put me about 1/4 of the way to completion. No problem: there are no technical show-stoppers.

The software seems to be the bigger unknown project, and will of course become a perpetual project after launch. Wary of the unknowns, I'm working hopefully toward splashing the first complete OneFish2 AUV late 2017.
