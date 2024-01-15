#### reasoning
it is a set of process that provide the basis of judgement and making predictions

#### learning
it is the activity of gaining knowledge by studying and practicing 
learning is categorized into various types 
- Auditory (by listening and hearing)
- Episodic (remembering sequences)
- motor (by movement of muscles )
- relational (it involves learning to differentiate various stimuli on the basis of relational properties)

#### problem solving
it is the process in which one perceives and tries to arrive at a desired solution from a present situation by taking a path blocked by known or unknown hurdles 
it also includes decision making which is the process of selecting the best suitable alternative out of multiple alternatives to reach the desired goal
#### perception
it is the process of acquiring interpreting selecting and organizing sensory information
perception presumes sensing in human perception is aided by sensory organs
but in the domain of ai the data is acquired in a meaningful manner

#### linguistic
it is ones ability to learn comprehend speak a language
it is important in interpersonal communication

#### diff between human and machine intelligence
- human perceive by patterns where as a machine perceives by data
- humans store and recall info by pattern but machines do it searching algorithms
- human can figure out the complete object even if some part of it is missing
- but the machines can do it correctly if we are providing explicit data 

### what is an agent and structure of agent
** **
#### what is an agent:-
an agent can be anything that will perceive an environment (sense)
and after sensing it acts on the environment
through actuator
**there are 3 types of agent**
- human agent
- robotic agent
- software agent

#### agent environment:-
**types of environment**
- ==***fully observable vs partially observable***:-==  if an agent sensor can sense or access complete state of an environment then it is fully observable environment else it is partially observable 
- ==***static vs dynamic environment***:-== if the environment can change itself then it is known as dynamic otherwise it is static. static environment are easy to deal with by an agent. but the dynamic environment need high end intelligent agent.... automatic vehicle driving is an dynamic agent but any puzzle solving game is an static agent
- ==***discrete vs continuous*** :-==  if an environment there are a finite number of percepts and actions then it is known as discrete else it is continuous 
- ==***deterministic vs stochastic:-***== if an agent's current state and selected action can completely determine the next state of the environment then such environment is called deterministic..... a stochastic environment is random in nature and cannot be determined completely by an agent  
- ==***single agent vs multi agent:-***==   if only one agent involved in an environment then it is known as single agent environment.... yk the multi one cmon man...
- ==***episodic vs sequential:-***==  if there is a series of one shot action and only the current percept required for the action to complete then it is episodic.. an agent requires the record of past actions.. i.e. sequential agent
#### Turing test:- 
`The Turing Test, proposed by Alan Turing, assesses a machine's ability to exhibit human-like intelligence. In the test, a human judge engages in text-based conversations with both a human and a machine. If the judge cannot reliably distinguish between the two based on their responses, the machine is considered to have passed the Turing Test. While it's a historic benchmark, passing the test doesn't necessarily indicate true intelligence, and modern AI research explores various capabilities beyond conversational skills.`
the model depends on an interrogator who decides between a chatbot and a human responder and it is observed if the chatbot can outperform the human counterpart 

###### features required to pass turing test
---
- ==NLP:-== nlp is required to communicate with interrogator 
- ==Knowledge representation:-== it is used to store and retrieve info during the test
- ==machine learning:-== it can detect the pattern
- ==vision and motor control unith==
#### types of agent:-




#### assignment 1 : collect the example of each agent that is working on each environment (9/1/23)
```It seems like you're referring to different types of agents that operate in specific environments. Agents can be various entities, such as software programs, robots, or even humans, that interact with and operate in specific environments. Here are examples of different agents in various environments:

1. **Software Agent in a Computer Environment:**
   - *Example:* A chatbot that assists users with customer support on a website.

2. **Autonomous Robot in a Physical Environment:**
   - *Example:* A self-driving car navigating through city streets.

3. **Human Agent in a Social Environment:**
   - *Example:* A customer service representative assisting customers over the phone.

4. **Industrial Robot in a Manufacturing Environment:**
   - *Example:* An automated robotic arm assembling products on a factory assembly line.

5. **Autonomous Drone in an Aerial Environment:**
   - *Example:* A drone used for surveillance or package delivery.

6. **AI Trader Agent in a Financial Environment:**
   - *Example:* An algorithmic trading program making stock market decisions based on market data.

7. **Virtual Assistant Agent in a Virtual Environment:**
   - *Example:* A virtual assistant, like Siri or Google Assistant, providing information and performing tasks on a smartphone.

8. **Search Engine Agent in an Information Retrieval Environment:**
   - *Example:* Google's search engine algorithm indexing and retrieving information from the web.

9. **Medical Diagnosis Agent in a Healthcare Environment:**
   - *Example:* An AI system analyzing medical data to assist in diagnosing diseases.

10. **Game-Playing Agent in a Gaming Environment:**
    - *Example:* An AI player in a video game, like AlphaGo playing the board game Go.

These examples cover a range of environments and types of agents, showcasing how different entities operate and interact within specific contexts.
```

in a goal based agent is uncertain about which path it will take but the utility based agen find the best path and explore the path 

learning agent:- a learning agent has mainly 4 conceptual learning agent
1. learning element
2. critique 
3. performance element
4. problem generator

1.it is reponsible making for making imporvement from learning 
2.here the leaning element takes feedback from critique which describes that how well the agent is doing with respect to a fixed performance standard 
3.it is responsible for selecting external actions
4.this component is responsible for suggesting action that will lead to new and informative experience 

difference between weak ai and strong ai

#### weak ai
 -it is limited to perform some specific task 
- programmed for fixxed funcs
- no consciousness and awareness 
#### stong ai
-it performs intelligent ai activities
- has the ability to learn think and perform new activities like humans
- it posseses creativity common sense and logic like humans


## searching in ai
---
the search algorithm in ai provides solution to many artificial intelligence related issues
##### search algo terms:-
- search
- search space
- start state
- goal state
- search tree
- action
- path cost
- optimal solution
