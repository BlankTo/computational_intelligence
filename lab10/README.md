first i tried with the montecarlo approach playing only vs random player (like prof did in the dedicated lesson), adding only the functions to extrapolate the moves from the dictionary obtained. File: lab10_montecarlo.ipynb

then i tried to add to the training matches against the player itself. The results were similar but the time to create the player each time increased significantly (in my implementation at least). File: lab10_montecarlo_2.ipynb

i also tried to add symmetries, but without good results. I think because of some error i made in the code (to be honest i hadn't time to debug it properly). File: lab10_montecarlo_symm_discarded.ipynb

then i tried with minmax, which was much more slower until i added a dictionary of (state -> move) to speed up the process. the dictionary is filled while the minmax compute the max_value of each state in depth. If some states are not considered in the initialization, they are added to the dictionary while playing. The results are better and the algorythm is very fast. File: lab_10_minmax.ipynb


Finally, i checked who would win between montecarlo and minmax. The result is a draw (i kept 1000 games by mistake, but there is no random, so each game is equal). File: lab_10_montecarlo_vs_minmax.ipynb