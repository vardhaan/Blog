# AR UX


## Overview

AR promises to be different. With it, we can finally bridge the gap between the worlds of bits and atoms. Our reality becomes electronic, and with that, it becomes computable and manipulable. But current UX practices aren’t ready for this. What does a cursor look like in the real world? How do you interact with an object physically and digitally at the same time? 

We are going to explore what makes AR UX different from our current standard for screens. Then, we’ll discuss ways we can make excellent UX for AR.


## Why is UX important?

User eXperience (UX) is what the user sees and feels while using a product. Users won’t use boring, unintuitive, complicated products if given the choice. This is understood by pretty much every tech company. Well, almost every tech company (looking at you, Workday).

AR companies are, and should be, focused on hardware and overcoming physical constraints. There’s still lots of work to be done in batteries, displays, and heat sinks before AR glasses are comfortable, powerful, and safe. However, it is impossible that only one company will figure this out[^1]. At that point, we can expect multiple companies to release AR glasses within a year of each other. Then, good UX becomes table stakes: among similar options, users will choose the AR glasses with better UX.

In fact, bad UX can hurt products even with no competition. Google Glass was the only product of its kind in 2013. Yet it flopped spectacularly. Among other factors, it had horrendous UX — users had to strain their eyes upwards to even see anything. And good luck navigating through screens.

So, getting AR UX right will be crucial to users, who want easy products, and to 1P companies, who want to win the market. Additionally, good UX standards baked into the OS and hardware make it so much easier for 3P devs to build good experiences on the devices.

However, getting AR UX right will take a lot of experimentation and work. We can’t just port over our current practices because of many fundamental differences.


## Why will AR UX need to be different?

**The real world is the screen. **Physical safety is not guaranteed. Clicking a button on a phone screen will do no physical harm to you. But interacting with a physical object (say a metal sign) could. Additionally, digital overlays may occlude real objects. Not seeing a car coming at you because a digital ad occluded it may be life-or-death.

**The display isn’t touchable.** Picture how smudgy and dirty AR glasses would get if people touched the lenses all day long. All current mobile UX assumes a touchscreen. Laptop/desktop UX doesn’t assume that but the use cases are different from those of AR’s; AR will be on-the-go.

**Social stigma limits interaction models. **Imagine seeing someone in public swinging their arms wildly and gesticulating to no one in particular. You would probably give them a wide berth or avoid them altogether. This is what people may think when they see you using hand gestures for AR glasses; social stigma limits the use of this interaction model.

**Sparseness is mandatory.** Imagine trying to even walk down the sidewalk if your entire field-of-view was covered with digital overlays. Facebook messages, Yelp recommendations, and TikTok videos could obstruct your vision. Alternatively, imagine you’re on a date. How annoying would it be if LinkedIn pulled up your date’s profile (or everyone in the bar’s profile) every 15 seconds or every time you glanced around. You’d hardly be able to focus and before you know it, the date is over with no shot of a second one. 

Current mobile UX assumes your phone is the main focus of your attention. There can be buttons and red notification bubbles everywhere. Every pixel is designed to catch and keep your attention. AR UX cannot make that assumption — people will be using it throughout their day as a supplement to their main activities. So. information overlays must take as little space as possible and must come only when needed. Otherwise, users’ FOV will be cluttered and it’ll be harder to function in the real world.

**Experiences must be predictive.** This is tied closely to the above point. Information must come only when it’s needed. Mobile UX relies on users explicitly asking for information when they need it (e.g. through search). But AR has the benefit of context—all the sensors and cameras on the glasses are there to estimate context and predict what information the user wants at that time. However, getting these predictions right will be extraordinarily hard. If a user is looking at storefronts on a busy street, do they want information about the storefronts? If so, which one[^2]? Even for a particular one, do they want the menu and recommended items or do they want hours and reservations? We will need tons of contextual information (e.g. who you’re with, the time of day, your implicit preferences, etc.) to get predictive experiences right. We struggle with it heavily even with one-location devices such as Google Home. Solving this will be one of the greatest challenges the tech industry will ever face.


## Principles of Interaction

So, we will need new interaction models for AR. For that, we must remind ourselves of the basics: the fundamental principles of UX and interaction.

**Intuitive.** A good UX should feel natural. A user should not have to think about navigating within an app/experience or about the mechanics of selecting an object. Unintuitive interactions are hard to remember and hard to remember means no repeat usage.

**Efficient.** Interactions shouldn’t take much energy to do. It would be tiring to have to swing your whole arm just to swipe left or right on your phone. The less energy needed, the more you can do it. Additionally, you’re less likely to encounter social stigma with more efficient movements.

**Sensical.** The interaction movement must make sense for the action. Selecting an object shouldn’t require a swipe-down. This also helps counteract social stigma. Random, herky-jerky movements look crazy. Fluid points and swipes look like technology interactions.

**Visual field == Interactive field. **This isn’t a de facto standard but I think it will be paramount for AR. It means that you can directly interact with what you see just with your body. This doesn’t apply to computers. There, the visual field is the screen and the interactive field is the mouse/trackpad. They are at 90º from each other and need a cursor to map between each other. Imagine having to use a cursor to interact with the real world. That would break immersion pretty quickly.


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

**Discreet Mode: **Here, your attention is not primarily on the digital experience. You may be navigating somewhere, on a date, networking, or countless other things. This is where AR promises to shine, by providing you information that helps you in your primary activity (e.g. helping you remember people’s names & occupations at a networking event). However, you’re likely to be in public here and social stigma matters. This means that the UX has to be discreet. You don’t want to get distracted and you don’t want others to think you’re distracted either. This limits the interaction models to those that look like natural, non-distracted movements. Additionally, the UX here has to be sparse and predictive, as mentioned before so that you get only the information you need without distracting.


## Good Interaction Models

There are two good interaction models that really make sense for AR glasses, one corresponding to each mode above. They follow the UX principles listed previously. They also are achievable in the short-term. Let’s take a look.

**Hand Tracking: **AR glasses (using their built-in cameras) can track the position and orientation of your hands. You can then use your hands to interact with objects in your FOV. This will be the dominant interaction model for Main Focus Mode. Here are some examples:



* Select an object — point at it with your hand / grab it with your fist / tap it with your finger
* Move an object — move your hand to where you want the object to go
* Zoom in — grab the object with 2 hands and pull diagonally
* Rotate an object — make circles with your finger

**Gaze Tracking: **Outward and inward-facing cameras can track where your eyes are looking. You can then use gaze to interact with objects. This will be the dominant interaction model for Discreet Mode. Here are some examples:



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

**Brainstorm**



* Aka, how will we interact with AR glasses?
    * Brainstorm list:
        * Eye motion
        * Facial motions
        * Brain computer interface
        * Speech 
        * Throat motions
        * Finger motions
        * Physical controller
        * Shaking the head
        * Blinking
        * Things we reach out to/touch
        * Twitching our feet
        * Magnetic implants in our fingers
        * Moving our mouths slightly
        * Physical controller that’s also a status symbol
        * Watch
        * Maybe the glasses will interact with us, we don’t need to control them
        * Lifting weights
        * Staring at a fixed point = put cursor there
        * Swipe to unlock
        * Left hand palm is a control surface
        * Tongue motions
        * Our phones (but only the touchscreen)
* What is a user’s mental model for interaction?
    * Discreet
    * Energy efficient
    * Don’t need extra accessories
        * This is important — there should be no risk of bringing the headset but not being able to use it because you forgot the accessory.
        * At the very least, the accessory should be built into the headset.
    * Feedback
        * Why is this important? Helps users know that their action was registered and received by the system.
    * Smooth (linear interactions, not 0-1)
    * Phone interaction standards will be what users think of first
    * Low latency
    * High precision
    * Degrees of freedom
    * Intuitive (follows what we do naturally, with real physical objects)
    * Interaction should not be the focus (assuming there’s good content. If no good content, then delightful interaction can help).
    * Cursor or not?
        * Seems like a cursor is necessary when the visual field and the interactive field aren’t the same. (e.g. you can’t tap on the computer screen, you need to use a mouse but a mouse’s plane of use is infinite whereas the computer screen is finite).
    * Also, the interactions will need to be compatible with existing web content.
    * What are the basic interactions?
        * Select an object
        * Text input
        * Move an object
        * Scroll
        * Remove an object (speed of removal must be high. P0)
    * What is special about the AR headset compared to other computing devices (in terms of interaction)?
        * The real world is interactable
        * You cannot tap on the display (glass)
        * There are tracking cameras
        * People may not know if you’re interacting with the headset
        * Compute power onboard will be limited at first
        * Most interactions will be quick. People aren’t going to be scrolling long webpages while walking around.
            * Relatedly, most interactions won’t be deep. A quick “continue” or “dismiss” may be the majority of cases. Why?
                * People are using these glasses while doing other things (e.g. talking to people). They don’t have mental bandwidth to be searching for items or deep interaction.
                * On second thought, these use cases will be what AR glasses uniquely enable but they may not be the majority. People still might use their glasses as they would a phone (focusing on the phone’s content at the expense of their surroundings).
                    * Someone might scroll reddit on their headset while they walk.
                * Do people multitask with their phones?
                    * Among my friend group, not really. They either focus on their phone or on something else. Not both.
* Should interaction design be tailored towards different use cases or have a holistic philosophy?
    * Why can’t it be both?
    * I think bottoms-up followed by coalescent top-down is a good approach.
* Transience is key. For many use cases, we don’t need information to persist longer than it takes someone to read it.
    * Time-boxed info — disappears automatically after X seconds. 
        * Downside is this puts the user in a race against time to consume information.
    * Eye focus — if user reads it then looks elsewhere, dismiss.
        * Downside is user may not think looking elsewhere means dismiss.
    * Opt-in to info — a user has to open up the info box. The info box will then persist until the user chooses to close it.
* For more persistent use cases (where the user consciously chooses it), how will we go about that?
    * The same movements I bet.
        * Why? Otherwise it takes thought on the part of the user.
* Eye focus is important. We don’t want transient information about everything in the environment popping up.
    * Whatever you’re looking at should be the thing that gets information popped up.
* Given this mental model, what modalities work?
    * Phone as a touchscreen
        * Not that discreet
        * Easy for users to pick up — same motions as they already do
        * However, if I want to select a small icon in the upper right of my FOV, how do I know where on the phone touchscreen to tap?
* What is the framework at play?
    * What are the underlying principles?
        * Interaction should be easy and second-nature.
    * Intuitivity is learnable but the more intuitive headset is the one that will get bought, all other things equal.
    * The interaction should fade into the background — your brain shouldn’t have to think about it.
    * You don’t want to look like you’re fidgeting or crazy (e.g. wild hand gestures). This is ok on a phone because people know you’re interacting with the phone. They may not know you’re interacting with your AR headset.
    * The interaction should be energy-efficient. It shouldn’t require a whole arm movement to move something or zoom in.
    * Should interactions be atomic? As in, not often interrupted.
    * Visual field == interactive field? Why is this important?
        * Feels more intuitive. 
        * If your goal is to augment reality, putting a cursor there breaks immersion.
        * OTOH, don’t controllers become part of the body? Doesn’t our mind quickly adapt to using them?
        * I think people also expect to be able to manipulate objects in AR directly.
* It seems like using hands to control will be very important. But discreetness is lost with hands.
    * When is discreetness needed?
        * When in public or when focusing on multiple things.
* What about typing?
    * Eye swyping
    * Hand tracking
    * Speech
    * Choose character or word? 
        * The standard is choosing characters on a keyboard. So replicating that speed is important. But also, it may be some time before users need to type a lot on AR glasses.
    * What if we use GPT-3 to come up with good responses automatically?
* How do we do eye movements?
    * Stare at something to click on it
    * Move your eyes Left-Right to dismiss something. Up-Down to click on it. This hurts eyes though. People don’t have muscles like that.
    * Make small motions with your eyes. I actually think motions are easier when there’s a line for the user to follow.
        * But what about people with eye problems? Eh we can deal with that later.
        * Will we need a cursor for the eyes? Doesn’t have to be a traditional cursor. Could just be a laser pointer to show where the system thinks your eyes are looking.
            * But this sorta defeats the point of not having a cursor so that visual field == interactive field.
        * People won’t need a cursor because people know where their eyes are pointing.
    * Maybe the eyes focusing tells the system where the user is focusing. But the user can wear a little ring with a button to actually click.
        * This seems less attractive though — the system isn’t self-contained.
    * How do we distinguish users looking at certain points for more info vs. daydreaming/staring into the distance/or even looking at something in reality that happens to be there?
        * Maybe the ways their eyes are focused vs. unfocused
    * With eye tracking, interactions are harder. You can’t have actions nested 4 clicks deep because it will take effort for the user to get there.
* What about neuro-modalities? E.g. Sensors that detect if your neurons fired so you can click without having to actually move your fingers.
    * We are very far from this. But can the same be said of eye tracking and hand-tracking technology?
        * No, I think those are both a lot more advanced.
        * Angular error for Gaze estimation is 3º (SOTA). At a distance of 5m, that’s 0.4m radius of error.
* Haptics / feedback will be an issue
* Let’s focus on intuitive and efficient.
    * Eye movements
        * Very efficient — you move your eye an inch, you’re looking at a completely different part of your FOV.
        * Intuitive — your eyes indicate focus automatically
* The user experience is important for AR glasses adoption.
    * Google Glass suffered poor UX. This in part led to its failure.
    * There are many different companies working on AR glasses — UX will be a key differentiator for them.
* UX will be novel for AR glasses.
    * The real world is the screen. 
    * The display isn’t directly touchable.
    * There may not be visual indicators that someone is using AR glasses.
    * Clutter will be deadly.
    * AR glasses will need to be predictive, not reactive.
    * Interaction has higher costs.
* Principles of interaction
    * Intuitive
    * Efficient
    * Sensical
    * Interactive field == visual field
        * Otherwise breaks immersion
        * For computers, the digital world is immersed in the screen. For AR, the physical world is the screen so making it too digital breaks immersion.
* Two modes of AR — discreet/multi-tasking vs. solo focus
    * Discreet — public, doing other things. This is truly where AR shines, bringing information to you as you need it.
    * Solo focus — this is like having a weightless phone. Still cool, but not the main reason to get AR.
* The two modes of interaction
    * Gaze-tracking
    * Hand-tracking
* Gaze tracking
    * CV-based, angular error up to 3 degrees
    * What would this look like?
        * Looking at points to interact
        * Looking away from points to de-focus them
    * Issues
        * Unintentional looking
        * Overlays on environment need to be carefully selected
        * Depth / are you looking at background or overlay
        * Haptics
* Hand tracking
    * CV-based
    * What would this look like?
        * Rays from hands for distant objects
        * Actual manipulation with hands for near objects
    * Issues
        * Depth
        * Your hands vs. someone else’s hands
        * Can require energy
        * Not accessible
        * Haptics
* Other interfaces
    * Neuro
        * Thoughts vs. actions
        * Privacy
    * Voice
        * No one uses it
        * Social stigma
    * Physical controller
        * Likely the near-term choice
        * Feels like a video game
        * You’re not interacting with the real world though.

<!-- Footnotes themselves at the bottom. -->
## Notes

[^1]:
     Even if only one company figures it out, other companies will copy or “be inspired” from them.

[^2]:
     We can’t show information about every storefront at once. That would violate our principle of sparseness. There are UX ways around this, though, as we will see later.
