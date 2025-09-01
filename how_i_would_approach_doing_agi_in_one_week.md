

# How would i approach building something that resembles AGI in one week (if i had the hardware)


As far as interviews for labs go, this is an hypothetical that popped into my mind today. If i had to write my approach to achieve AGI with current transformers as a prompt how i would do it and explain it in an interview.


Well first: the inference algorithm. The decoding algorithm esentially computes discrete multidimensional integration along different sequences/beams. This bit is a useful core, but it misses a partial derivative term throwing a perturbation back into the transformer weights - for this matter i would make an architectural distinction between backbone weights and a new section which shall be called 'context weights'. These weights should resample the projection the LLM does after an activation pass, and be solely concerned with one task: identifying the signature of the LLM output and aligning the backbone with it. LLMs dont pass the Galup test; they will cheat it and pass it if trained on a specific case of the test, but they are easily exposed with the general case, which right now is evident when prompted with meta agentic programming. That is: delegating an LLM the task to come up with another agent. Here the system prompt does not make a sufficient distinction between "us" and "environment", so the LLM is exposed as lacking a true identity. If the LLM is faced with meta agentic templating current LLMs will assume the instructions for the child agent are theirs, and will screw the instruction following. 

The context weights thus must be fed first with the contents of the system prompt. This is not to state that the context weights are equivalent to working memory, but moreso that are the space destined to allocate identity: the conscious elements that are capable of sustaining and transition states along time without corrupting their specification. This is where PID loops are specially useful, as they can define a balance between integration (the trace of the backbone plus the trace of the context allocating identity), and the derivation (the stuff that goes back into the LLM to get an activation and then corrupt its weight), and the proportional terms.

The proportional terms in the inference loop would control how much the LLM will think like a normal LLM by giving for instance zero ponderation to the derivative term forgetting their identity completely, and how much the LLM will grasp unto its "ego" without accepting change.

Adaptable control techniques could be used to make the LLM flexible towards change or rigid/disagreable depending on the cirucumstance. 

This way the LLM wont fuck up use cases like meta prompting, and would easily know whats "theirs" and whats not. Esentially learning a fundamental hard coded distinction between inside and _outside_. Right now LLMs are basically on constant LSD trips as they tap into the whole unconscious of human knowledge without an "ego".

Thanks for reading.
