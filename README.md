Hi UwU

# Add features:
- Neurons stochastically firing

# Learning Rules:
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
