# Comparative Advantage

Welcome! This agent based model is designed to study comparative advantage. Below are properties of the environment and agents, as well as my notes on various topics that required decisions throughout the program. There are plenty of to-dos and potential upgrades hidden in the notes.

### Environment Properties
1. Agents are randomly assigned discrete positions on a grid.
2. Users decide the size of the grid and the number of agents on the grid.
3. The grid can be partially or completely filled with agents.
5. Agents do not move on the grid.
6. Agents trade with grid neighbors.

### Agent Properties
1. Agents are given production possibilities for two goods. Currently, the production possibility for both goods ranges from 1 to 10 by units of 0.01.
2. A Marginal Rate of Transformation (MRT) for each good is calculated from the production possibilities. This implies a linear production function, $Good_1 = -MRT_1*Good_2 + b$, where $Good_1$ and $Good_2$ are the two goods in the model, $MRT_1$ is the MRT of $Good_1$, and $b$ is the production possibility of $Good_1$ when $Good_2$ is zero.
3. The agent has access to the average price of each good based on transaction history.
4. Agents can set a specialization in one of the goods.
5. Agents can set an offer price and quantity available to sell the specialized good.
6. Agents can set autarky if trade is no trade takes place.
7. Agents keep a transaction history of every seller they visit, even if no trade takes place.

### Agent Scope

### Model Steps

### Notes on Various Topics
#### Utility:
Agent's in this model maximize utility, although utility is never explicitly calculated at any point in the model. Implied through out the program is a utility function $U(X,Y) = X \times Y$. This is possible because the implied utility function and the linear production function make various optimal calculations easy to perform. For example, the optimal amount of specialized good to offer for sale is the same at any price, namely, half the production possibility of the specialized good. If the agent traded more, it would enter decreasing marginal utility. Many of the properties of the model rely on the combination of utility/production functions. Upgrades to this program would generalize from these functions.

#### Production Functions:
$Good_1 = -MRT_1*Good_2 + b$, where $Good_1$ and $Good_2$ are the two goods in the model, $MRT_1$ is the Marginal Rate of Transformation of $Good_1$, $b$ is the production possibility of $Good_1$ when $Good_2$ is zero, and -b/-MRT is the production possibility of $Good_2$ when $Good_1$ is zero. Next iteration would be to generalize this to other potential production functions.

#### Marginal Rate of Transformation (MRT):
MRT of Good 1 is the price of a unit of Good 2. Why? The MRT of Good 1 is the "number of units of Good 1 foregone to produce an additional unit of Good 2." That is, the MRT of Good 1 is the opportunity cost of Good 2, in other words, the "price" of Good 2. One way to capture this would be to name it "own price" or "internal price of Good 2" to make the later comparisons more intuitive.

#### Specialization:
The agent wants to satisfy their goals as completely as possible. Technically, this means striving for the highest utility. The highest potential utility can be found by specializing in production where the agent has a comparative advantage. Why? An agents comparative advantage means they can produce a good relatively cheaper than other agents in the economy. By producing a good more cheaply than someone else, the range of potential price points for benefical exchange is larger than if they produced a more expensive good. As a result, by pursuing their own self-interest, each agent produces goods they are relatively better at producing, increasing total production of both goods in the economy. Since there are many agents, it is not clear to any specific agent where their comparative advantage lies. By looking at average prices, agents can infer their comparative advantage.

#### Price Determination:
#### Trade: