# DrugForge: RL for Drug-like Molecule Generation

Implements and evaluates a reinforcement learning framework for de novo molecular generation, where molecules are represented as SMILES strings and generation is formulated as a sequential decision making problem. The goal is to optimize the QED while preserving chemical validity and structural diversity. A two-layer LSTM-based SMILES language model is first trained via maximum likelihood on approximately 200k molecules from the GuacaMol dataset, providing a chemically informed prior with ~90% validity. RL is then applied in SmilesRLEnv using both REINFORCE and PPO with an actor–critic architecture, where the terminal reward is the QED score computed by RDKit. The results demonstrate that RL can substantially bias molecular generation toward drug-like chemical space under a strong SMILES prior, while highlighting the exploration–exploitation tradeoff and the need for explicit diversity regularization when using powerful policy optimizers such as PPO.

<img width="900" height="614" alt="QED-PPO" src="https://github.com/user-attachments/assets/1f70598a-1d9e-46a7-9a47-2632fbbc9103" />

This is a final project for Stanford CS238, Autumn 2025. Full version of project report and discussion could be found in the course website: https://aa228.stanford.edu/old-projects/.
