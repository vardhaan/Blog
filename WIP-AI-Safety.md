<!-- Yay, no errors, warnings, or alerts! -->


# AI Safety

**Overview**

Overall, AI Safety is harm reduction. A medical diagnostic AI model shouldn’t send someone in for an operation if they don’t need it. A language AI model shouldn’t say something offensive. A image classifier shouldn’t misidentify humans as gorillas. Harm can be physical and emotional.

Long-term AI Safety is existential. If/when we develop AGI (Artificial General Intelligence), we will need to ensure they don’t view us as an enemy or as subordinates. However, this is decades off and not what **all** our focus should be on.

Instead, short and medium-term AI Safety is dangerous in its own right. Harm here looks like misclassifications or inappropriate responses. But, with AI models already being used in law, finance, and health, simple errors by the model have already lead to disastrous results. Even your Alexa saying “Democrats are stupid” is harm enough. We need to focus more on minimizing harm here.

**A quick mental model**

The most important factor for AI model safety is scope—where and how a model is used. If a model has limited scope, then Safety is not paramount (though still important). For example, if an AI model is used to differentiate between types of flowers and a human reviews every classification, then the model getting some wrong is no big deal. However, if the scope is large (such as deciding whether a person should get bail, as COMPAS does), then any error can drastically change people’s lives. Those errors, compounded, can change the whole legal system.

Ideally, we want to use AI models in high-scope situations. At any given scope, it’s then quality of training that determines the model’s safety. Quality of training is a loaded phrase though. It refers to many things: quantity of low-error training data, compute time available, well-designed objective functions, optimal model architecture, and so on. I spent a year on this stuff and I still feel like I only scratched the surface.

Here’s a table to summarize:


<table>
  <tr>
   <td>
   </td>
   <td><strong>Low quality training</strong>
   </td>
   <td><strong>High quality training</strong>
   </td>
  </tr>
  <tr>
   <td><strong>High scope</strong>
   </td>
   <td>Extremely harmful
   </td>
   <td>Low harm, but be vigilant
   </td>
  </tr>
  <tr>
   <td><strong>Low scope</strong>
   </td>
   <td>Bad model, but irrelevant
   </td>
   <td>Unharmful, let it run
   </td>
  </tr>
</table>


**Current state of Safety**

Pretty much every FAANG company and research university has teams working on AI Safety. Companies that sell AI models focus on reducing their harm. But it’s a nascent space. When I worked on AI Safety, I was shocked that there wasn’t a solution I could just plug into. And this was at Google no less.

I expect an explosion of effort in AI Safety over the coming years. However, research here will be constrained to wealthy institutions. This fact, combined with computing trends, will leave a massive gap in AI Safety.

**The Safety Gap**

AI models will have harmful impacts in the next 5-15 years because they will be democratized.

Democratization is a Universal Law in AI. What was the cutting edge 5 years ago is a building block today. What required a whole team of PhDs to discover 5 years ago is accessible via an API call today. What took 3 weeks to run 5 years ago runs in an hour today. This Law is pretty much driven by two things:



* Increase in training power and speed
* Developer incentives

_Increase in training power and speed_: Moore’s law is just the start. Every week there’s a new development in GPUs, AI-focused chips, AI model architectures, and large training sets. On the MLPerf benchmark, AI model performance has 8x-ed in just 3 years.

_Developer incentives:_ developers are motivated to share their findings, either through free open-source software and libraries or through paid APIs. Image convolutional neural nets required a PhD to set up just 10 years ago. Nowadays, they can be trained via an API call to keras.fit().

I expect the same will happen in the future. The large language models we see now will likely follow a similar path, especially as research focuses on making them more efficient and smaller to train and store. In parallel, advances in processors will make it feasible for smaller companies to develop their own models. Financially, this makes sense for a company: instead of having to pay high marginal cost for an off-the-shelf model and still having to finetune it, they can build their own model for more fixed cost but no marginal cost. And, as we said, that fixed cost decreases every year.

However, AI Safety won’t be guaranteed if companies develop their own models. Quantity of training data is still AI’s biggest bottle neck and most companies don’t have the time to focus on quality. This will leave a small gap in AI Safety for that one company or developer. However, replicate this across many companies and industries and we suddenly have **a massive problem**.

**How do we solve this?**

We can solve this either through improving training or decreasing harmful results. Behavioral economics tells us that the latter resonates more; it’s easier to see negative impacts than to see positive potential. It’s also likely that smaller companies have less knowledge and resources to commit to training. But decreasing harmful results requires only financial capital.

The two main options for decreasing harmful results are to:



* Release integrated AI models that are all-in-one: deployable and Safe
* Release Safety models that complement the client’s AI model

_Release integrated AI models:_ Here, we would release our own building-block AI models (e.g. fully deployable LLMs, CNNs, etc.) that are also trained on Safety. A client would just have to finetune this model on their data and deploy it.

_Release complementary Safety models:_ Here, we would focus on models that detect Safe and Unsafe outputs. The client would build their own model (e.g. through keras), send their models’ responses to us, and our model would mark any Unsafe outputs.

However, the first option naturally lends itself to a library. That’s a fragmented space — many a competent AI developer can release a library of high-performing AI models. Libraries are generally not funded well either and AI Safety is an arms race. It requires ongoing investment.

The second option, however, allows us to focus on key differentiators. And key differentiators are necessary if we want people to use our product (even if it’s a non-profit). What’s the point of having a revolutionary AI Safety model if no one uses it? Additionally, it taps into the trend of AI DIY (and low/no-code in general). It’s also cheaper for the developer to only have to pay for Safety as opposed to the whole AI model plus Safety. Lastly, we could iteratively expand our product to option 1 over time. 

**Why will this approach work?**

Safety problems differ by domain (e.g. Safety in computer vision is vastly different from Safety in text generation). But, within each domain, there are only a few overall problems. For example, in text generation, figuring out the Safety of a sentence within context is the main issue. Most companies’ needs for the AI models don’t differ too much either. If you solve the Safety problem for one company in a domain, you’ve likely solved it for quite a few others.

Additionally, Safety is often immediately table-stakes. If everyone’s model is Unsafe, then there’s little pressure. However, if even one competitor’s model is Safer than yours, then there will be high pressure to make yours Safer.

However, the main reason this approach works is because 

**Integrated models vs. not**

Is it better to have 1 model that’s been trained on both performance and Safety or is better to have 2 models, 1 trained for performance and 1 trained for Safety? Personally I think it’s better to have the 2 models — easier to debug for sure. Also, that’s how effective brainstorming works for humans (double diamond approach). It does take more compute time and effort though to have 2 models.

Will the industry tend towards vertical integration? I suspect so. Mostly because of precedence. Damn near every industry goes through phases of bundling and unbundling. But what is necessary for successful vertical integration? The benefit - cost has to be higher over time w/ VI than without. Why do companies vertically integrate? It helps them build more powerful, specialized products at lower costs (and higher margins), often for a wealthy buyer/consumer. It’s a key form of differentiation. However, you do lose some specialization — your focus is now on more than 1 area. If we build out a product that is a complementary Safety model, some opportunist will think to launch a product that’s an integrated Safety model. And B2B buyers will wonder why they need to have 2 models when they can just have 1.

**Will AI become DIY?**



* Training will become easier and cheaper.
* However, cutting edge performance will never be DIY. But, will we reach a performance threshold where additional performance is not as valuable as price? We are already there in some domains (e.g. digit recognition).
* People adopt DIY when acceptable performance is available but for a lot cheaper. For internal stuff, this would def hold true. For things where SLAs are involved, they may want the heavy-duty off-the-shelf items unless they have considerable expertise in-house.
* Mid-sized tech companies don’t have this considerable expertise in-house. However, they also don’t need cutting edge stuff. The best way to answer this would just be to ask them.
* Other CS disciplines followed a similar path. Web dev started out very complex but then frameworks were developed and released that made it easy for any dev to pick up. Same with graphics, etc. Yet there are still web dev agencies and consultancies for clients that can’t or don’t want to do the web dev work.
* Honestly, I don’t know what companies do right now. I know FAANG companies develop their own. If I was in charge of a smaller company, I’d probably copy what FAANG companies do. If another company provided those models to me, I’d pay for them.
* In the longer-run, I’d expect more developers and companies to do DIY (especially for already-proven models—AlexNet is now a commodity). For those, they’d probably want to stick with FOSS or they’d expect the models to have Safety built in.
* What about APIs? Companies may want to use SOTA models but don’t want to pay for it. Well I don’t think they’d want to purchase 2 models (one SOTA performance model and one Safety model). They’d want it all-in-one.
* Really, the business here might be to sell Safety models to existing AI model companies.

**Will AI model companies prioritize Safety?**



* For classification models, Safety is performance. Errors in classification usually fall under Fairness. On top of that, Safety issues here relate to context of use. The model by itself could be fine but the feature it’s launched in makes it Unsafe. Safety of the model itself is less of a concern here. Unless the feature-space is limited, the AI model company can’t account for all the potentially Unsafe ways a Safe model might be used.
* For generative models, Safety is unrelated to performance (unless you have wonky performance criteria). High-performing models also have the ability to become Unsafe (that’s what makes them high-performing). Here, the model can be Unsafe without context. Thus, clients would care more about the model being Safe by itself. So, a good AI company would prioritize Safety here.

**Is it ethical to charge for AI Safety?**



* By charging, you’re only allowing certain companies to have access to Safety. Concentrated but deep impact. If you release FOSS, everyone can get access but you may not have the funding to solve harder problems. Diffuse but shallow impact.
* Perhaps one can do both — free Safety software for most companies and unique products for paying companies.
    * This doesn’t seem very venture-backable? But it does remind me of what a lot of SaaS companies do.

**Safety issues are fixed**



* It’s mostly judging whether outputs are harmful or not. The space of outputs is generally fixed too; sentences are sentences, whether said by a human or an AI. AIs outputs will approach humans, but we can already train on humans.
* Safety detection problems, then, are fixed in size. Detecting whether a certain output is harmful or not is not complex and doesn’t differ case-to-case. Of course, there will be some variance (e.g. some GPT-3 features can tolerate vulgarity or not) but these are solved with toggles in one system, not with different systems for each case.
* What about bad actors? There will always be people trying to break models. One argument is that they’ll want to go after the big fish (FAANG, even sklearn). But any vulnerabilities there will be fixed ASAP. The smaller fish (smaller tech companies making their own models) won’t be as rewarding. The other argument is that doing high-volume attacks on smaller companies will net more reward since they’re less protected and one attack may work on many. However, with Safety, it’s more about reputation and less about money (although one’s reputation could be held ransom for money). But tbh, even DIY AI will likely derive from frameworks (sklearn, keras). 
    * This is a separate topic but will frameworks incorporate Safety into their models? Or will DIY AI devs have to use another framework/model or will they be left completely to their own devices?

**How will AI frameworks tackle Safety?**



* This comes back to integrated vs disjoint models (1 model or 2).
* Developing Safety independently is conceptually easier. Probably easier to motivate a team as well, since improvement can be constant. In an integrated model, you’d see Safety gains at the expense of performance losses and vice versa.
* LLMs tackle Safety with an integrated model — the model itself picks the least toxic response out of the generated candidates.

**So how would making a product for AI model companies work?**



* The expertise would really be in data collection & annotation. They know how to make their own AI models.
    * Honestly, it seems like they could do the data collection too.
* Is Safety specialized enough that AI model skills/human capital couldn’t work on that just as effectively?
    * I’d assume no, it’s still a mathematical and data problem. Although, there is a philosophical/social sciences/ethics portion of it.

**Will LLMs become a monopoly, oligopoly, or fragmented? What will determine which model(s) become the winners?**



* What will be the adoption of LLMs? Will it follow a similar path to ConvNets, etc.?

_~~Motivation to learn: This phrase may sound odd, since it gives a human characteristic to a machine. However, this is an underlying presumption for AGI. If a model can learn on its own (i.e. it pulls its own training data and trains itself), then we no longer control it. At this point, the model’s intentions and scope come into sharp focus. But, since we aren’t close to models with this ability yet, we can ignore it for now.~~_



* What are the problems with AI Safety?
* Why should we care about these problems?
    * How big will these problems get?
    * Will AI become democratized?
* Is Safety something that can only be dealt with by the model makers?
* How does competition factor in here?
* Is there money to be made in this space? How will that affect it?

Problems with AI Safety:



* The overall problem is harm: will AI harm humans and human institutions?
* Existential threat — what if AI harms humans?
    * Does it have to do it knowingly? Because otherwise you could argue toxic LLMs are harming humans.
* The current problems with AI safety focus on a model unintentionally causing harm.
* I think intentional vs. unintentional harm is a focus here. An AGI that goes against its training is intentionally causing harm.
* Scope of harm is also important. A model that has access to many domains and actions could cause a lot of harm unintentionally and still be an existential threat.
* Models today are very narrow in scope so the harm they do is very limited. At most, feelings get hurt. Of course, humans decide the scope so that can change. Also, AI doesn’t have to be an AGI to have big consequences. Things like COMPAS can silently degrade society if they were trained improperly. Having many models like COMPAS, all in different domains, all independent of each other, could have massive consequences.
* Bad training data
    * Isn’t this the core problem right now? AI basically goes based off its training data.
* Bad ratings/corrections
    * This is secondary to the training data because the training data is the anchor point for the model. We will never pick up on all the implicit patterns the model finds from the training data. So, corrections won’t help us fix those.
* Out-of-distribution attacks
    * In language models, subtle changes to the input query can cause drastic changes to the output. This makes for a great attack vector.
* Intentionality is related to ability to learn. If a model can’t learn things on its own, then controlling it = controlling its inputs. If a model can seek out learning on its own, then intentions (and capabilities/scope for harm) become important.

How big are these problems?



* Existential threat is, well, existential. If that doesn’t get solved, the consequences may be life-ending.

Will AI become democratized?



* Yes and no.
    * Yes — there are many, many pre-trained models that people can download and use and maybe do some finetuning on. Plus, there are AI methods that don’t require inordinate amounts of power and money.
    * No — large model creation is still stupidly expensive. And large models seem to be the way things are going: the more parameters, the better performance.
* In order for these smarter, larger models to become democratized, either the models must become smaller without sacrificing lots of performance. Or, server and training costs have to go down, by a lot.
    * Deepmind’s RETRO model is only 7 billion parameters (compared to GPT-3’s 175 billion) yet still performs just as well.
    * I predict an increase in size until we reach some crazy level of performance. After we understand what drives that performance, we will see a focus on efficiency and size reduction.
* The main question for whether democratization will exacerbate safety problems is: will the democratized models be from select, high-quality sources or will it be everyone creating their own models?
    * For simple (what does simple here mean?), it will probably be devs creating their own.
    * For complex models, it will be devs taking something off-the-shelf and finetuning it.
    * Eventually, though, complex will become simple. It may even just become a method in a library to train a Transformer.
    * For tech companies, they may want to continue investing in their own models since using off-the-shelf would lower their margins.
    * A big assumption I initially made iis that off-the-shelf models already have Safety baked in. This may not be true, or it may not be adequate. Even GPT-3 wasn’t all that safe. They had a content filter but it still said some nasty things. But then again, I haven’t heard much about bad things GPT-3 said in quite a while (I also haven’t heard about the model itself in quite a while, so it may not mean much).
        * Companies w/ fewer resources than FAANG may not be able to focus on Safety by themselves.
* The main issue with working on Safety is whether or not to provide the models that we do Safety on. How do you make 3P models safer?
    * You can prune unsafe results out. This would allow client companies to focus on other aspects of performance.
        * Client’s model would be able to generate whatever it wants. Our model would then filter out all the bad responses. Client’s model then picks the best option from the remaining responses.
    * You can parse through the training data and remove the bad aspects.
    * You can consult for the 3P. Help them develop the models.

One of the reasons to have a Safety-focused AI company is that Safety is an arms race. You can’t think of it once and then never again. The AI could itself become unsafe or there could be bad (human) actors undermining you.
