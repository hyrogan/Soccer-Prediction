# Soccer match outcome prediction with priors

### Problem definition of the Bachelor Thesis

Soccer is the most popular sport in the world. Consequently, statistical modelling of outcomes in soccer matches is popular among researchers (Scarf and Rangel 2016). While many papers focus on extensions to the Bradley-Terry model (Tsokos et al. 2019), in this thesis I will imple-ment a rating system based football prediction model proposed in the paper “Dolores: a model that predicts football match outcomes from all over the world” (Constantinou 2019) and then ex-tend it with additional factors to further improve it. Dolores is a model that first computes a rating difference between two teams based on a rating system and then calculates the 1X2 probabilities based on the rating difference through a Bayesian Network. Bayesian approaches seem promis-ing and have recently been used to compute in-game probabilities in soccer (Robberechts et al. 2021). In order to evaluate the extended model it will be compared to the basic version of the model and evaluated based on various factors as described below. There are four possible procedures:

(i)	A simplified basic model (Dolores without the Bayesian Network)

(ii)	A full basic model (Dolores as described in the paper)

(iii)	A simplified extended model (the simplified model with an extended rating system)

(iv)	A full extended model (Dolores with an extended rating system)

In a first step the rating system of the model has to be implemented. For the sake of simplicity we will ignore the Bayesian Network for now and try to reproduce the results of the original paper by substituting the Network with a probability distribution such as in Poisson Models (Maher 1982; Dixon and Coles 1997). The results of this simplified basic model are then compared to the ones of the Dolores model as found in the paper. At this point first conclusions can be drawn. 
If the results of the simplified model are similar to the ones of Dolores, then the Bayesian Network part of the original model will be excluded from this point on. This results in having more time to work on extensions for the model. Therefore, we will then build upon the simplified basic model. In this case we will compare the simplified basic model (i) to the simplified extended model (iii) in the evaluation step.  
On the other hand, if we can’t reproduce the results in this manner, it can be concluded that the Bayesian Network is a fundamental part of this model and therefore has to be implemented as well. In this case the extensions will be built onto the full basic model. This results in a comparison of the full basic model (ii) to the full extended model (iv) in the evaluation step. 

In the extension step more factors will be added to the rating system. It is part of the assignment to find such features that improve the prediction accuracy of the model. One idea is to include a luck factor for each team, which tries to illustrate how lucky a team has been over a certain amount of time by comparing the expected goals (xG) to the actual results. This factor would then to a certain degree be compensated to based on the assumption that past luck doesn’t translate to being lucky in the future. This is only one idea and others will need to be explored.

Once the extended model has been developed it is time to predict the outcome of future matches. This is usually done by choosing a timeframe and one or multiple competitions. The outcomes for all the matches in these competitions is then predicted and afterwards analyzed. As the model is able to predict the outcome of a game in which two teams play against each other solely based on their rating difference without relying on the data of previous matchups between the teams, it would be interesting to try and predict the outcome of international games. In these international games the two teams have often rarely played each other in the near past and therefore their outcome is usually hard to predict. You would assume that this model is perfectly suited to predict such games.
In the end the extended model has to be evaluated. This will be done by comparing its accuracy and Rank Probability Score (a measure of performance for probabilistic forecasts) to the ones of the non-extended model. The resulting probability predictions of the extended model can also be compared to betting odds for further conclusions. 


References
Constantinou, A.C. (2019). Dolores: a model that predicts football match outcomes from all over the world. Mach Learn 108, 49–75. https://doi.org/10.1007/s10994-018-5703-7

Dixon, M. J., & Coles, S. G. (1997). Modelling association football scores and inefficiencies in the football betting market. Applied Statistics, 46(2), 265–280.

Maher, M. J. (1982). Modelling association football scores. Statistica Neerlandica, 36(3), 109–111.

Robberechts, P., Van Haaren, J., & Davis, J. (2021). A Bayesian Approach to In-Game Win Probabil-ity in Soccer. Proceedings of the 27th ACM SIGKDD Conference on Knowledge Discovery & Data Mining, 3512–3521.

Scarf, P. & Rangel, J. S., Jr. (2016). Models for Outcomes of Soccer Matches. In J. Albert et al. (Eds.), Handbook of Statistical Methods and Analyses in Sports, 341-354.

Tsokos, A., Narayanan, S., Kosmidis, I. et al. (2019). Modeling outcomes of soccer matches. Mach Learn 108, 77–95. https://doi.org/10.1007/s10994-018-5741-1


