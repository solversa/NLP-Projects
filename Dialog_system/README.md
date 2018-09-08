# Dialog system categories
- Task-oriented (in closed domain)
- Non-task-oriented (i.e., chat bots, in open domain)

# 1. Task-oriented
## 1.1 Pipeline
  - NLU -> Dialog state tracking -> Policy learning -> NLG
  - NLU: maps the utterance into semantic slots
    - Domain: text classification
    - Intent: text classification (We can incorporate preceding text information during perform classification, see [8])
    - Slot: sequence labeling
  - DST: estimates the goal at every turn
  - PL: generates next action, can be done by supervised learning or reinforcement learning
  - NLG: convert action to utterance
## 1.2 End-to-end
  - ...
## Reinforcement learning
  - Entity: **agent** and **environment** 
  - Rule: agent takes **action** and environment gives **reward** and **state**
  - **Policy**: a rule that the agent should follow to select actions given the current state
# 2. Non-task-oriented
- 2.1 Retrieval  
  - Given pre-defined responses, retrieval based model predict one response given current input context [2].
  - Two steps [3]:  
    - retrieval top-k response candidates by directly matching
    - reranking and give best by incorporing context
- 2.2 Generative  
  - Generative new responses from scratch [2].

# Leading Researchers
- [Minlie Huang](http://coai.cs.tsinghua.edu.cn/hml/dataset/)
- [Rui Yan](http://www.ruiyan.me/)
- [Nan Duan](https://www.microsoft.com/en-us/research/people/nanduan/)

# Implementation
- [ChatterBot](https://github.com/gunthercox/ChatterBot) supplies a framework for building chatbot, and [Awesome-Chatbot](https://github.com/fendouai/Awesome-Chatbot) gives a list of public repositories about chatbot.
- [wxpy](https://github.com/youfou/wxpy), [wxBot](https://github.com/liuwons/wxBot), [WeRoBot](https://github.com/offu/WeRoBot): weChat bot.

# References
[1] [A Survey on Dialogue Systems: Recent Advances and New Frontiers](https://arxiv.org/pdf/1711.01731.pdf)  
[2] Deep Learning for Chatbots [part 1](http://www.wildml.com/2016/04/deep-learning-for-chatbots-part-1-introduction/), [part 2](http://www.wildml.com/2016/07/deep-learning-for-chatbots-2-retrieval-based-model-tensorflow/)  
[3] https://c.m.163.com/news/l/180148.html?spssid=fba792c95ad60299db5435a91da37e10&spsw=1&spss=other.  
[4] [A Network-based End-to-End Trainable Task-oriented Dialogue System](http://mi.eng.cam.ac.uk/~sjy/papers/wgmv17.pdf), and [implementation](https://github.com/shawnwun/NNDIAL), Ali Xiaomi  
[5] [End-to-end LSTM-based dialog control optimized with supervised and reinforcement learning](https://arxiv.org/pdf/1606.01269.pdf), [Hybrid Code Networks: practical and efficient end-to-end dialog control with supervised and reinforcement learning](https://arxiv.org/pdf/1702.03274.pdf), and [implementation](https://github.com/voicy-ai/DialogStateTracking)  
[6] [Learning End-to-End Goal-Oriented Dialog](https://arxiv.org/pdf/1605.07683.pdf) from Facebook, and [implementation](https://github.com/vyraun/chatbot-MemN2N-tensorflow)  
[8] [Sequential Short-Text Classification with
Recurrent and Convolutional Neural Networks](https://arxiv.org/pdf/1603.03827.pdf)
