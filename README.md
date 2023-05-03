# Validation Steps
- Remove LMAN, see what happens
- See if Hebbian Weights change to something intresting 

# Add features:
- Neurons stochastically firing
- For now, HVC is not an a psuedo RNN (monotonic input), recieves one-one syllable input (weights frozen at one)
    - later make it an RNN that can learn syllable length via RNN self sustainment 
- For now, LMAN doesn't even have a noise normal distrubtion just activations downstream Area X

# Learning Rules:
- For now, reward is equal to -MSE
- Area_X -> LMAN (none, all are 1s)
- HVC -> RA (hebbian)
- HVC -> Area_X ( Delta HVC-X = L_man_i( fired or not) * Reward * Learning Rate)

# Algorithim:
- HVC -> RA -> RA_output
- HVC -> Area_X -> LMAN (random normal for now)
- calculate reward
- RA_output = RA_output + LMAN bias 
- Hebbian update
- HVC-Area X update 

# Open Questions:
- How does LMAN learn to produce the right bias?
- Come up with plausible learning rules for AreaX -> LMAN
- DLM role and how to model inhibition to it 
- Timing, since the generation circuit part is way smaller 
