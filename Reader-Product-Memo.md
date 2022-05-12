# Reader Memo

**Overview**



* Focus on engineers who read, in companies
* Needs: understanding, remembering, focus, and enjoyment
* Chrome extension to summarize, focus, and enhance any document
* Writing is the real moat

Reader will dramatically enhance the document reading and writing experience. We will focus on making documents 10x more enjoyable, understandable, and distraction-free. This will allow users and their companies to think better, increase productivity, and even uplevel their overall creativity. In the white-collar world, these advantages differentiate the winners from the losers.

**Users**



* B2B
* Readers first
* Bottoms-up
* Engineers

We will focus on B2B users over B2C users since B2B users have strong incentives to optimize their document experience. A better document experience can make them more knowledgeable, help their projects succeed, and get them promotions. By doing so, users can gain knowledge, mastery, prestige, and money. These drill into four of the core human desires.

Within B2B, the market is along two axes: readers/writers and top-down/bottom-up. 

We will initially focus on readers and 10xing the reading experience; readers are both more exposed to new reader experiences (users consume multiple blogs, outside of work) and less picky (when’s the last time you didn’t read a document because it wasn’t in Notion?). However, the real user value and moat will be in capturing the writers market. Network effects really take off with writers highlighting the value of our product to both writer peers as well as their own audience.

We will focus on a bottom-up strategy. There is little incentive for an exec to purchase or mandate better document tools without showing an impact on the bottom line. But, upward pressure from users within the company will strongly mitigate this effect. If a company’s PMs are all using a certain product to read/write documents, then execs (along with everyone else) will look to them as the pulse of the company.

Engineers are the natural user group to focus on within a company. They comprise the most hours spent reading per year of any non-exec group in the company. Additionally, they are the most important department within tech companies, so demand from engineers for our product can lead to adoption at large. They also spend a decent amount of time writing themselves (mostly design docs and thought-out comments). Lastly, engineering culture tends towards efficiency. Products that can help in that direction will win out. We aim to do just that.

**User Needs**



* Understanding the points of a document
* Remembering the points of a document
* Not losing focus while reading a document
* Enjoying reading a document

These problems apply not just to engineers, which will greatly help us expand from department to department within companies. 

The key purpose of using a document is to enable a thoughtful discussion on a potentially complex topic. However, people aren’t good at writing. That makes reading hard. On a macro level, this is mostly bad logical flow, unsubstantiated arguments, or complicated examples. On a micro level, this can be incorrect syntax, obtuse vocabulary, or plain bad grammar. Any of these is enough to take a user out of flow or to spend less time thinking through the veracity and implications of the proffered arguments.

Understanding is the key need. But if you don’t remember what you understand, you might as well have not read the document at all. [The Forgetting Curve](https://www.csustan.edu/sites/default/files/groups/Writing%20Program/forgetting_curve.pdf) shows people forget 75% of what they learn within a day. This is not a problem inherent to documents, but it is a problem that no document experience has even attempted to solve.

Focus helps with the above two needs. Users can read a document while distracted, but they find themselves reading the same section over and over again. Unsurprisingly, this leads to poor understanding and poor memory. This is especially important in B2B since topics are complex; nuance and insight from every person may be required to solve a company-threatening problem. 

Lastly, enjoyment is missing from a lot of today’s document-based work. Superhuman is worth near $1B from making email fun. We can do the same for documents. If users _enjoy_ reading (and writing) documents, that will start a virtuous cycle of more documents being created and consumed (at higher speeds too). This cycle increases the productivity of the team. Even more importantly, it can dramatically increase the creative output of the team.

These needs are **not** adequately met with today’s reading experiences. Most reading experiences focus on getting out of the reader’s way. This has been because AI has been too underpowered and inaccurate to solve these problems. However, the wave of Large Language Models (LLMs) — like GPT-3, LaMDA, and GPT-J — enable us to dramatically reduce these pain points **now**.

**Proposed Solution**



* Automatic summaries as you go (Macro Understanding, Remembering, Enjoyment)
* Complex sentence substitutions (Micro Understanding)
* Smart distraction-free mode toggle (Focus)
* Visual autonomic arousal focus points (Focus)

We are not re-imagining the core of the document. There will still be typeset characters on the screen, aligned to margins, font sizes, etc. Imagine all the features as additions to your standard Google doc.

Summaries can now be done accurately; LLMs are excellent at summarizing inputs. We will show a summary of the overall points at the beginning of the document. This helps prime the reader. As the reader goes through the document, we highlight the summary of the section they are on. This enables mini-spaced-repetition, a proven way of increasing memory. It also enables the reader to understand the thesis that each sentence in the section ties back to. Additionally, this is a reward to the reader as well — reaching the next section highlights the next summary point, allowing the user to feel progress being made. We can show this highlight in a delightful way or even have muted visuals to accompany.

LLMs are also good at understanding and rephrasing sentences (they’re excellent at most language-related tasks). We will use this ability to show clean, clear alternatives to poorly-written sentences. This will enable a user to make sure they understand simply by reading the original sentence and the alternative that immediately follows it in parentheses.

Next, we will offer a built-in toggle to the product allowing the user to go into distraction-free mode on their device. This will last just for the time they read the document, so they won’t deal with the cognitive load of undoing distraction-free mode.

Lastly, we will leverage neuroscience protocols to enhance reader focus. In the brain, mental focus follows visual focus. Focusing on a certain point for 30-60 seconds leads to your brain then focusing on that point. We will start every document reading with a focus dot on the screen. In the future, we could use eye tracking (with strong user consent) or sound tracking to detect when a user might have lost focus and bring them back to their focus zone.

This reading experience will start off as a Chrome extension since that can operate on every document a reader looks at.

These features directly improve the four key needs of understanding, remembering, focus, and enjoyment for the document reading experience. However, they weren’t really doable until now with the emergence of LLMs.

**Moat and Roadmap**



* Turn readers into writers
* Team has extensive experience with LLMs
* Ideological difference from competitors
* Unlimited supply of documents

The biggest moat for this product will come when we focus on improving document writing. When a writer begins to use our product, they will be passing on the benefits (even more accurate summaries, clearer writing) to both their readers as well as peer writers. This can be exponential, with a k-factor potentially much higher than 1.

In the short-term, we have a moat with technology. Even though LLMs are becoming more ubiquitous, there is a very small set of people who know how to really maximize their outputs. The founder of the team has worked with LLMs extensively (on Safety) and is very familiar with prompt engineering, a key component for this product to work.

As mentioned before, competitors such as Google Docs and Notion usually leave the reader on their own. No tangible benefits have been possible for the reader until LLMs. However, this leaves those products with a vested interest to keep the interface clean since that is what their users have come to expect. We do not have such a limitation and we are free to chase other user niches.

Lastly, the fact that this is a Chrome extension means we can operate on any document (even any website) that a user accesses. Users won’t have to go to reader.com and import their document. This means an effectively unlimited supply.
