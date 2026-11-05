Quant-Projects
Volatility adjusted positions and order postings

Quantitative portfolio optimization with inspiration from schur components and quantum particle compositions

min-max strategy - forecasting

SQRT strategy - statistical patterns

Full-order-book multi-agent simulator with learn-to-trade RL bots

Meta-learning framework that hot-swaps models intraday based on entropy of live features

probabilistic-programming risk engine with automatic adjoint greeks

self-supervised alt-data miner that converts web/noise into trade-ready factors

differentiable back-tester with gradient-based strategy search

adversarial market-impact model trained on billions of historical prints


# WTECH
This repository is used for the algorithmic trading done with the startup company WTECH.

Below are some notes, sporadically written down to later be organized into the above folders.


Build your ideal state strategy. Where if in this state you will earn as much as possible.

Detect market state and opponent positions. - Because in general you're just playing against the market, but you're also playing against specific opponents.

Match market state with tactic to progress towards strategic goal points. - For each market state, there's a series of actions you can perform to go to your ideal state.

Decide on counter-measure or alignment-measure. - Depending on whether you're progressing towards your ideal state or moving away, you can take actions to move towards it again. a. If counter-measure, decide on size, direction, time and method b. If alignment-measure, decide on size, direction, time and method.

Proceed to optimal execution, considering market impact, timing and cost. - To best progress towards your ideal state, you can try to minimize cost or consider the best steps.

## possible improvements

* Run Leveraged trades
* Run options, futures and swaps
* Run multiple asset types: Crypto, equity, derivatives, commodities

Algorithmic trading on medium time horizons

HFT - market making

Investing and venture capital on a long time horizon

Banking insurance and pension

Robotics, IT and resource development
energy

Macrostrategy

Detect Market state

What is the current trend state?
Question:
How precise is the mean return functional at detecting the trend?
How precise is the positive-negative functional at detecting the trend?
How precise is the battery of statistical tests at detecting the trend?

What is the current risk state?
Question:
What's the current volatility states?
What's the current connectability in the market?
What are the current probability states?

Has an extremal event occured?
Question:
How precise is Bollinger bands of 1.5, 2 or 2.5 sigma at detecting Extremal events?
How precise is the 10%, 5% and 1% quantile of xyz-interval returns at detecting Extremal events?
How precise is the 10%, 5% and 1% quantile of xyz-interval prices at detecting Extremal events?

Match corresponding strategy
If Up trend:
run long between 0-tangents, to minimize risk of loss
Check for Extremal events
If Negative Extremal event occurs - Close trades, take loss. Halt trading
If Positive Extremal event occurs - Close trades, take profit. Gauge trading
Check for Divergence and weight of closed trades.
If open, high and low diverge over time.
Consider whether a high volatility period is ahead and how to benefit on buying low and selling high.
If the the weight of the closing trades are significant and a certain direction has been chosen.
Consider whether to play along the direction or to take profit before a direction change.
Check for moment and moment drift
If Down trend:
run short between 0-tangets, to minimize risk of loss
Check for Extremal events
If Negative Extremal event occurs - Close trades, take loss. Halt trading
If Positive Extremal event occurs - Close trades, take profit. Gauge trading
Check for Divergence and weight of closed trades.
If open, high and low diverge over time.
Consider whether a high volatility period is ahead and how to benefit on buying low and selling high.
If the the weight of the closing trades are significant and a certain direction has been chosen.
Consider whether to play along the direction or to take profit before a direction change.
Check for moment and moment drift
If Flat trend:
run long between 0-tangents, to minimize risk of loss
run short between 0-tangets, to minimize risk of loss
Check for mean reversion indications
If the 6, 20 and 40 day moving averages cross
If the average directional index changes
If the trend indicators change
If the autocorrelation indicator increases
Check for Resistance levels If the Price reaches a previous resistance level - concrete price If the price reaches a fibonacci level - mythical & mystical price level If the price drops by x% from a previous max or min
Check for Breakthrough signals Unsure how to check this at the moment
If unknown trend:
Wait till a clear trend manifests
Implement trading strategy
If - Up trend
Entry:
Exit:

If - Down trend
Entry:
Exit:

If - Flat trend
Entry:
Exit:

If - Extremal event
Entry:
Exit:

Optimal executions
Up trend
Entry:
Exit:

Down trend
Entry:
Exit:

Flat trend
Entry:
Exit:

Research
DATASET - Price Timestamp+Date Open High Low Close Volume Returns_C

DATASET - Options

Markov model/Decision Tree Research
Goal: Determine the sign of tomorrows return, from today's Markov State.

Train the model on n > 25 datasets.
a. Sort dataset by conditions. for us this is up MA-cross and down MA-cross - This has to be researched further.
b. Add column with "Up" or "Down" indicators. Indicating the sign of the day's return.
c. Add column with indicator combinations of 3 and 5, such as "UUU", "DDD" and "UUUUU", "DDDDD".
d. Calculate the probabilities of next day return signs for each indicator combination.
Test the model, with the goal of achieving x >= 65% accuracy.
a. The current mean accuracy is 55% ...
If the result is x < 65% -> than there exists hidden variables. a. There must exist hidden variables, unaccounted for in moving averages
Hidden Markov model Research
Goal: Determine the trend, volatility, acceleration and sentiment states for tomorrow.
From a dataset on an asset. Determine the combined state for each timestep.
Question: How will I make the system decide on a given state?
Given 4 trends states: Up, Down, Flat, Unknown.
Given 4 volatility states: Extreme, high, medium, low.
Given 4 acceleration states: increasing, decreasing, neutral, Unknown.
Given 4 sentiment states: Positive, Negative, Neutral, Unknown.

Mean reversion Research
Goal: For periods where Mean Reversion is valid, what is the best method for earning?
What method is best at predicting mean reversions?

MA5, MA20, MA40
MACD
A combination?
Convergence Theorem Research
Goal: Determine the convergence or divergence states for high, low and close prices

Calculate convergence or divergence of highs
Calculate convergence or divergence of lows
Calculate convergence or divergence of close

What can this be used for? Market states, 0-tangents?
Linear Regression Research
Standard Deviation Research
Can you always or nearly always expect an opposite and equal force, when experiencing an 2-sigma, 2.5-sigma or 3-sigma event?

Mean Field Games Research
Technical Indicators Research
Expectation Maximation Research
0-tangent Research
How do i best measure 0-tangents, vendetangenter?

f(x) = Price f'(x) = returns f'(x) = 0?

Event based HFT
When Token X goes from Pumpfun to Raydium. Buy with HFT and sell. Pumpfun raydium? dexscanner Jito fees? spamming/crowding

Sandwich/MEV bot

KuCoin

Other
lgb, xgb, catboost https://www.kaggle.com/code/aimind/bottleneck-encoder-mlp-keras-tuner-8601c5

Cross-Validation (CV) Strategy and Feature Engineering:

5-fold 31-gap purged group time-series split Remove first 85 days for training since they have different feature variance Forward-fill the missing values Transfer all resp targets (resp, resp_1, resp_2, resp_3, resp_4) to action for multi-label classification Use the mean of the absolute values of all resp targets as sample weights for training so that the model can focus on capturing samples with large absolute resp. During inference, the mean of all predicted actions is taken as the final probability Deep Learning Model:

Use autoencoder to create new features, concatenating with the original features as the input to the downstream MLP model Train autoencoder and MLP together in each CV split to prevent data leakage Add target information to autoencoder (supervised learning) to force it to generate more relevant features, and to create a shortcut for backpropagation of gradient Add Gaussian noise layer before encoder for data augmentation and to prevent overfitting Use swish activation function instead of ReLU to prevent ‘dead neuron’ and smooth the gradient Batch Normalisation and Dropout are used for MLP Train the model with 3 different random seeds and take the average to reduce prediction variance Only use the models (with different seeds) trained in the last two CV splits since they have seen more data Only monitor the BCE loss of MLP instead of the overall loss for early stopping Use Hyperopt to find the optimal hyperparameter set

https://www.kaggle.com/competitions/optiver-realized-volatility-prediction/discussion/274970 https://www.kaggle.com/competitions/optiver-trading-at-the-close/discussion/487446 https://www.kaggle.com/competitions/jane-street-market-prediction/discussion/224348




Navn. Tomorrow
Type, High-frequency trading(technical), Low frequency trading(fundamental)
Requirements 40000 cash for ApS, ??? For A/S. 10. Mil for investment company
Depotselskab, bankkonto erhverv, hjemmeside, teknologi, it, lei-id 

Investeringsfond og kunde bank


Improvement points
Skal have mere styr på skatteregler, opbygge formue
	1. Investere i yty, yt3y, yt5y, profitable og gennemtænkte virksomheder med høj dividende.
	Køb under indreværdi, sælg over profitable værdi
	2. Tag fast beløb på 200kr Per år Per kunde. Sådan at ca. 100 kunder kan dække afgifter Per år
	3. Gør det hele til et “non-profit” scheme

Tomorrow 
Summary documents
Legal documents
Customer documents
Client documents
Analysis documents
Technical documents
Programming setup

Tomorrow holding
-investments fund
-ressources company
-learning institution, AI robots, AI predictive modelling, Library of everything

	

Machine learning
Is the field of study inside the study of artificial intelligence, where the focus is on statistical algorithms that can effectively generalize and thus perform tasks without explicit instructions.



Deep learning

Is a subset of machine learning, so statistical methods for generalized task performance.
They're usually artificial neural networks with representation learning.
Deep means multiple layers in the network, they're used to progressively extract higher-level features from the data input.


Artificial neural networks






Unsupervised learning(data driven)
Dimensionality reduction (structure discovery, feature discovery, visualisations of big data, meaningful compression)
Clustering ( recommendation systems, segmentation, targetted marketing)
prediction(?)


K means clustering
Mean-shift clustering
DBSCAN clustering
 (Gaussian)Mixture model
 Dirichlet process
Neural networks
Hidden Markov Model
(Agglomerative) Hierachical clustering

Supervised learning(task driven)
Classification/Regression/Estimation



Classification(diagnostics, customer retention, image classification, fraud detection)
Support vector machines
Naive Bayes classifier
Discriminate analysis
K - Nearest Neighbour
Neural Networks
Decision Trees
Random forest
Gradient boosting
Ensemble Methods
Nonlinear regression

Regression (popularity/growth prediction, forecasting, estimating life expectancy)
Neural networks
Decision Trees
Ensemble methods
Nonlinear regression
Linear regression
Support vector regression
Lasso regression
Ridge Regression
Logistic regression
ElasticNet Regression
SVR, RVR, GPR
Poisson Regression




Reinforcement learning(Decision-making)
Game AI, skill acquisition, learning tasks, robot navigation, real-time decisions

Algorithms that learn to react to an environment
Q-learning
R-learning
TD learning
DQNs
SARSA
DDPG

Artificial Intelligence?
Deep learning?


Keras
Tensorflow
Scikit-learn
pyTorch
XGBoost
NLTK
SpaCy


Turing test

chatbot

ChatGPT
https://chat.openai.com/

Image generation

Midjourney/DALL-E
https://www.midjourney.com/home?callbackUrl=%2Fexplore



Webcrawlers

Phind
https://www.phind.com/

Webcrawlers
https://www.webcrawler.com/


Google - plain and simple

	1. Planlægge programmets målsætning
		a. Skal kunne løse følgende problemstillinger
			i. Forudse fremtiden
			ii. Risikostyre imod fremtidige problemstillinger
			iii. Holde og danne overblik
			iv. Hjælpe med rapporteringer
			v. Hjælpe med regnskab
			vi. Auto data indlæse
			vii. Holde styr på kapital reserve
			viii. Premium beregninger
			ix. IRB
			x. Investeringsperformance
	2. Hvilke funktioner skal programmet opfylde
		a. Funktion 1
		b. Funktion 2
		c. Skal kunne vise relevante nyheder og brugbart "further your knowledge" mulighed
	3. Hvordan skal GUI være opsat.
		a. Design tema
		b. Sideplan, hvor skal hovedsiden lede hen og hvilke ekstra sider skal der være
		c. Hvordan skal man kunne få fat i funktioner
	4. Hvad kræves der for at programmet kan fungere korrekt.
	5. Hvordan skal kunderne betale for programmet.


SIRI - voice recognition
	1. Planlægge programmets målsætning
		a. Skal kunne løse følgende problemstillinger
			i. Forudse fremtiden
			ii. Risikostyre imod fremtidige problemstillinger
			iii. Holde og danne overblik
			iv. Hjælpe med rapporteringer
			v. Hjælpe med regnskab
			vi. Auto data indlæse
			vii. Holde styr på kapital reserve
			viii. Premium beregninger
			ix. IRB
			x. Investeringsperformance
	2. Hvilke funktioner skal programmet opfylde
		a. Funktion 1
		b. Funktion 2
		c. Skal kunne vise relevante nyheder og brugbart "further your knowledge" mulighed
	3. Hvordan skal GUI være opsat.
		a. Design tema
		b. Sideplan, hvor skal hovedsiden lede hen og hvilke ekstra sider skal der være
		c. Hvordan skal man kunne få fat i funktioner
	4. Hvad kræves der for at programmet kan fungere korrekt.
	5. Hvordan skal kunderne betale for programmet.

Bevægelses engine
Trades
Transaktioner
Invoices

Opbevarelse
Af bankingbook
Af investeringer
Af Capital
Af budget
Database til oversigt over
Kunder
Items
Trades
Transaktioner
Invoices
Investeringer
Policies

Utility
Noter
Pipelines
Datagruppering
Dataredigering
Messages

Dashboard og KPIer
Inddeling af system i forskellige lag
Grafer og visualiseringer
Forecasting og predictive analyse

Layer 1 - ledelsesinformation

Expenses, liabilities, assets, income

Dashboard, budget/balance sheet
Overview visualizations
powerBI-like

Simulation option
It should be possible to activate a simulation
Option, where certain scenarios can be simulated and decision-making can be tested

Real time option
It should be possible to activate or default to a real-time option, where current affairs are displayed

Coder's option
It should be possible to activate a coder's option, to customized the interface for each company without having to contact technical support and make a big show out of everything.

Has to be able to recommend interface setups with AI and possible optimizations of company with AI

Layer 2 - middle office and operations

Investments, loans, insurance policies, projects etc.
Portfolio structure, select a portfolio and overview its contents

Has to activate different analysis sublayers, depending on the type of portfolio.

Analysis sublayers

Use investment analysis
	Fundamental analysis for portfolio managers
	ESG analysis for ESG analysts
	Technical analysis for traders?
Use loans analysis
Use insurance analysis


Example:
To determine whether a purchase or sale is a good idea
Selling or buying an equity for a portfolio.
Selling or buying an insurance policy

Has to have a simulation option, real-time option and coder's option
For the same reasons as layer 1.

Must be able to apply optimization of portfolios with and without AI
Must also be able to apply newest analysis tools for pricing and hedging

Layer 3 - risk management and critical issues

-Has to have a fraud estimation function. To estimate whether a claim or transaction is fraudulent.
-Has to have a capital reserving function


-has to have a ruin process, to estimate whether the company will survive and stay solvent.
-has to have a claims process, to estimate the expected payout from the reserves over a given period of time
-has to have a premium calculation and credibility process
To estimate what amount of premium is expected for any given policy holder to achieve the given return.

-has to have an anti-money laundrering process.

-has to have an investment risk process, for which currency risk, value at risk, interest rate risk, derivatives risk and more has to be included
-has to have a default risk process for counterparties.
-has to have an allocation, ESG and diversification metric


Has to have a simulation option, real-time option and coder's option
For the same reasons as layer 1.


	1. Webdomæne med brugbart navn
	2. Hjemmeside
	3. Planlægge programmets målsætning
		a. Skal kunne løse følgende problemstillinger
			i. Forudse fremtiden
			ii. Risikostyre imod fremtidige problemstillinger
			iii. Holde og danne overblik
			iv. Hjælpe med rapporteringer
			v. Hjælpe med regnskab
			vi. Auto data indlæse
			vii. Investeringsperformance
	4. Planlægge UI og funktionaliteter
		a. Hvordan skal GUI se ud
			i. Design tema
			ii. Sideplan, hvor skal hovedsiden lede hen og hvilke ekstra sider skal der være
			iii. Hvordan skal man kunne få fat i funktioner
		b. Hvilke funktioner skal hjemmesiden have
			i. Investeringsportefølje

			ii. Typer af analyse

			iii. Skal kunne vise relevante nyheder og brugbart "further your knowledge" mulighed

			iv. Overblik over
				1. Trades
				2. Beholdninger
				3. Mulige instrumenter
				4. Portefølje KPI'er
			
			Mulighed for at
				1. Undersøge instrumenter med analyse værktøjer
				2. Undersøge KPI'er og portefølje
				3. Undersøge scenarier og simuleringer
				4. Søge information og nyheder
				5. Forum
			
			Dashboard og KPIer
			Grafer og visualiseringer
			Forecasting og predictive analyse
			
	5. Hvordan skal der betales for arbejdet?
	


Co-pilot
https://github.com/features/copilot
<img width="926" height="4046" alt="image" src="https://github.com/user-attachments/assets/51097bc2-84ef-4fc8-a699-9f180cd76d39" />





