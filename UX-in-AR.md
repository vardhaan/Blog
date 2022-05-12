# AR UX


## Overview

AR promises to be different. With it, we can fully bridge the gap between the worlds of bits and atoms. Our reality becomes electronic, and with that, it becomes computable and manipulable. But current UX practices aren’t ready for this. What does a cursor look like in the real world? How do you interact with an object physically and digitally at the same time? 

We are going to explore what makes AR UX different from our current standard for screens. Then, we’ll discuss ways we can make excellent UX for AR.


## Why is UX important?

User eXperience (UX) is what the user sees and feels while using a product. Users won’t use boring, unintuitive, complicated products if given the choice. This is understood by pretty much every tech company. Well, almost every tech company (looking at you, Workday).

AR companies are, and should be, focused on hardware and overcoming physical constraints. There’s still lots of work to be done in batteries, displays, and heat sinks before AR glasses are comfortable, powerful, and safe. However, it is impossible that only one company will figure this out[^1]. At that point, we can expect multiple companies to release AR glasses within a year of each other. Then, good UX becomes table stakes: among similar options, users will choose the AR glasses with better UX.

In fact, bad UX can hurt products even with no competition. Google Glass was the only product of its kind in 2013. Yet it flopped spectacularly. Among other factors, it had horrendous UX — users had to strain their eyes upwards to even see anything. And good luck navigating through screens.

So, getting AR UX right will be crucial to users, who want easy products, and to 1P companies, who want to win the market. Additionally, good UX standards baked into the OS and hardware make it so much easier for 3P devs to build good experiences on the devices.

However, getting AR UX right will take a lot of experimentation and work. We can’t just port over our current practices because of many fundamental differences.


## Why will AR UX need to be different?

**The real world is the screen.** Physical safety is not guaranteed. Clicking a button on a phone screen will do no physical harm to you. But interacting with a physical object (say a metal sign) could. Additionally, digital overlays may occlude real objects. Not seeing a car coming at you because a digital ad occluded it may be life-or-death.

**The display isn’t touchable.** Picture how smudgy and dirty AR glasses would get if people touched the lenses all day long. All current mobile UX assumes a touchscreen. Laptop/desktop UX doesn’t assume that but the use cases are different from those of AR’s; AR will be on-the-go.

**Social stigma limits interaction models.** Imagine seeing someone in public swinging their arms wildly and gesticulating to no one in particular. You would probably give them a wide berth or avoid them altogether. This is what people may think when they see you using hand gestures for AR glasses; social stigma limits the use of this interaction model.

**Sparseness is mandatory.** Imagine trying to even walk down the sidewalk if your entire field-of-view was covered with digital overlays. Facebook messages, Yelp recommendations, and TikTok videos could obstruct your vision. Alternatively, imagine you’re on a date. How annoying would it be if LinkedIn pulled up your date’s profile (or everyone in the bar’s profile) every 15 seconds or every time you glanced around. You’d hardly be able to focus and before you know it, the date is over with no shot of a second one. 

Current mobile UX assumes your phone is the main focus of your attention. There can be buttons and red notification bubbles everywhere. Every pixel is designed to catch and keep your attention. AR UX cannot make that assumption — people will be using it throughout their day as a supplement to their main activities. So. information overlays must take as little space as possible and must come only when needed. Otherwise, users’ FOV will be cluttered and it’ll be harder to function in the real world.

**Experiences must be predictive.** This is tied closely to the above point. Information must come only when it’s needed. Mobile UX relies on users explicitly asking for information when they need it (e.g. through search). But AR has the benefit of context—all the sensors and cameras on the glasses are there to estimate context and predict what information the user wants at that time. However, getting these predictions right will be extraordinarily hard. If a user is looking at storefronts on a busy street, do they want information about the storefronts? If so, which one[^2]? Even for a particular one, do they want the menu and recommended items or do they want hours and reservations? We will need tons of contextual information (e.g. who you’re with, the time of day, your implicit preferences, etc.) to get predictive experiences right. We struggle with it heavily even with one-location devices such as Google Home. Solving this will be one of the greatest challenges the tech industry will ever face.


## Principles of Interaction

So, we will need new interaction models for AR. For that, we must remind ourselves of the basics: the fundamental principles of UX and interaction.

**Intuitive.** A good UX should feel natural. A user should not have to think about navigating within an app/experience or about the mechanics of selecting an object. Unintuitive interactions are hard to remember and hard to remember means no repeat usage.

**Efficient.** Interactions shouldn’t take much energy to do. It would be tiring to have to swing your whole arm just to swipe left or right on your phone. The less energy needed, the more you can do it. Additionally, you’re less likely to encounter social stigma with more efficient movements.

**Sensical.** The interaction movement must make sense for the action. Selecting an object shouldn’t require a swipe-down. This also helps counteract social stigma. Random, herky-jerky movements look crazy. Fluid points and swipes look like technology interactions.

**Visual field == Interactive field.** This isn’t a de facto standard but I think it will be paramount for AR. It means that you can directly interact with what you see just with your body. This doesn’t apply to computers. There, the visual field is the screen and the interactive field is the mouse/trackpad. They are at 90º from each other and need a cursor to map between each other. Imagine having to use a cursor to interact with the real world. That would break immersion pretty quickly.


## Types of Interactions

There are just a few interactions that form the basis of the Interaction space.



1. Point
2. Click
3. Drag
4. Swipe
5. Type

If we can nail these, then building complex interactions (such as zooms, tab switching, etc.) become easy.


## Two Modes of AR

I think there will be two dominant modes of using AR: one where it’s the focus of your attention and one where it’s complementary to another experience. We must design for both of these since they have very different requirements.

**Main Focus Mode:** Here, your attention is primarily on the digital experience. This will be akin to having a phone/laptop in front of your eyes. You could edit documents, watch YouTube, or scroll TikTok. Usually, you’d be in private settings here so fear of social stigma doesn’t matter. So, more interaction models are possible here.

**Discreet Mode:** Here, your attention is not primarily on the digital experience. You may be navigating somewhere, on a date, networking, or countless other things. This is where AR promises to shine, by providing you information that helps you in your primary activity (e.g. helping you remember people’s names & occupations at a networking event). However, you’re likely to be in public here and social stigma matters. This means that the UX has to be discreet. You don’t want to get distracted and you don’t want others to think you’re distracted either. This limits the interaction models to those that look like natural, non-distracted movements. Additionally, the UX here has to be sparse and predictive, as mentioned before so that you get only the information you need without distracting.


## Good Interaction Models

There are two good interaction models that really make sense for AR glasses, one corresponding to each mode above. They follow the UX principles listed previously. They also are achievable in the short-term. Let’s take a look.

**Hand Tracking:** AR glasses (using their built-in cameras) can track the position and orientation of your hands. You can then use your hands to interact with objects in your FOV. This will be the dominant interaction model for Main Focus Mode. Here are some examples:



* Select an object — point at it with your hand / grab it with your fist / tap it with your finger
* Move an object — move your hand to where you want the object to go
* Zoom in — grab the object with 2 hands and pull diagonally
* Rotate an object — make circles with your finger

**Gaze Tracking:** Outward and inward-facing cameras can track where your eyes are looking. You can then use gaze to interact with objects. This will be the dominant interaction model for Discreet Mode. Here are some examples:



* Select an object — look at it for a few seconds
* Move an object — look at a specific section (an anchor section) of an object for a few seconds then look to where you want it to be
* Zoom in — blink twice in rapid succession / look at a specific section (a tool section) of the object
* Rotate an object — look at an anchor section then make a circle with your eyes

However, interactions will be limited in Discreet Mode. Most interactions will boil down to “dismiss” or “give me more information.”

Let’s delve further into these two models.


## Hand Tracking

**Why Hand Tracking?**

Above all, it’s intuitive. Your hands are designed for you to manipulate objects with. Sci-fi media has also reinforced the notion of using your hands to manipulate digital overlays (e.g. Tony Stark discovering a new element in Iron Man 2).

Because it’s intuitive, it’s also sensical. Someone seeing your movements would understand you were doing something on your AR glasses. 

It’s efficient, similar to how swipes and taps are efficient on phones. It doesn’t take much energy to move a few fingers or just your hand. 

Lastly, it equates the visual and interactive field. If you can reach out and “touch” objects, that is the gold standard of interactivity. There’s no cursor needed.

**How might this work?**

This section is speculative and consists of hypotheses on how Hand Tracking interactions could work.



1. Point: Point with a finger while keeping your other fingers relaxed. Raycasting (projecting a line from your finger in AR) can help you make sure you’re pointing where you want
2. Click: A slight forward motion of your hand while pointing at something.
    1. Alternatively, could be tapping your index and thumb finger together while pointing at something.
3. Drag: While pointing at something, keep that finger extended and somewhat slowly trace it to where you want the object to go. The object should follow smoothly along.
4. Swipe: Same as drag, but without pointing first. 
    2. Alternatively, could be 2+ fingers instead of 1.
5. Type: A virtual keyboard could be projected a few inches in front of the user, in the bottom third of their FOV. The user could make the same motions they would for typing on a normal keyboard. Or they could do Swype as on phones.

**Issues with Hand Tracking**



1. Detection errors: running hand pose estimation requires highly-trained computer vision models and good cameras. Even with these, there will be errors. SOTA models can keep error with 10mm though. So, this won’t be a notable issue except when pointing at far off objects when 10mm of error could lead to large angular divergences over large distances. Another type of error here is distinguishing between your hands and other hands. If multiple people, including you, are pointing in the FOV, which pair should the system focus on?
2. Depth errors: what if there was a digital overlay over a storefront and you pointed in that direction? Are you pointing at the overlay or at the storefront? The system will be unable to tell. This will be an annoying occurrence, but one that may not happen all too often since Hand Tracking is mostly for Main Focus Mode, which will happen in more private areas.
3. Haptics: you will not get any tactile feedback on your hands from clicking, dragging, or interacting in any way. The glasses themselves could vibrate to simulate that but it will not be the same. Gloves could solve this but they make a new problem — the AR glasses are no longer self-contained and you’d need to remember to bring the gloves.


## Gaze Tracking

**Why Gaze Tracking?**

Our eyes naturally look at things we’re interested in. So, we can take long gazes as a Yes signal and short/no gazes as a No signal. So, it feels intuitive.

It’s discreet as well. Even in conversation or presentations, looking around is normal. You’re not always looking the other person in the eye. So, if a digital overlay pops up on the right and you glance at it, it won’t look like you’re distracted. It will just look like normal eye movements.

It’s efficient because your eyes only have to move a few millimeters to complete interactions.

In Discreet Mode, which is where Gaze Tracking is important, quick information consumption is the primary interaction. “Learn more” or “Dismiss” will likely be the most common interactions. There, Gaze makes sense to choose one quickly.

Lastly, Gaze Tracking also equates the visual and interactive field. Where you look is where you interact. There is no gap.

**How might this work?**

This section is speculative and consists of hypotheses on how Gaze Tracking interactions could work.



1. **Point: Looking at any part of an object.**
2. **Click: Looking at any part of an object for an extended period of time (say 5 seconds).**
3. Drag: Looking at the anchor point for an object for 5 seconds then slowly looking to the desired destination.
4. Swipe: For any carousel/experience where scrolling is needed, have “buttons” on the edges of the FOV. Looking at a button for 5 seconds will scroll in that direction.
5. Type: Bring up a virtual keyboard and use Swype technology to input with Gaze.

Pointing and Clicking will be the most important interactions because users will be engaged in other activities while in Discreet Mode.

**Issues with Gaze Tracking**



1. Detection errors: Gaze Tracking also relies on complex computer vision models. SOTA performance has an error of up to 3º. For an object 5 meters away, there would need to be error buffers of 0.4m. This is roughly half a doorway in width. So, not bad as long as there aren’t many objects in the FOV.
2. Depth errors: Are you looking at the digital overlay or the real object that happens to be behind it? One potential solution may be in pupil dilation/aperture. This solution can also help with distinguishing between focused gazes and deep-in-thought blank stares.
3. Haptics: There will also be no tactile feedback on interactions here. Vibration of the glasses may help though.


<!-- Footnotes themselves at the bottom. -->
## Notes

[^1]:
     Even if only one company figures it out, other companies will copy or “be inspired” from them.

[^2]:
     We can’t show information about every storefront at once. That would violate our principle of sparseness. There are UX ways around this, though, as we will see later.
