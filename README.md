## Introduction

We replicate the paper by Ashwood et al. [ashwood2022mice] In perceptual decision-making, agents such as rodents and humans process sensory information to guide their choices. Traditional computational models, like signal detection theory [steckler2001using] and evidence accumulation frameworks [odoemene2018visual], have typically assumed that individuals apply a consistent decision-making strategy throughout an entire experiment. Recently, reinforcement learning (RL) models [luksys2009stress, bathellier2013multiplicative] have challenged this notion by proposing that agents dynamically adapt their strategies to optimize performance over time.

Despite these advances, current models still struggle to account for unexpected errors that agents commit even in seemingly straightforward trials with strong perceptual cues. These errors, known as "lapses," are generally viewed as sporadic mistakes due to temporary lapses in attention or memory. Standard modeling approaches, such as epsilon-greedy RL, typically assume lapses occur randomly and independently, assigning them a fixed probability (epsilon) where agents ignore available information and make arbitrary choices.

However, lapses may not simply be random events; rather, they could reflect abrupt shifts in underlying decision-making strategies. For instance, rodents might alternate between an "engaged" state, characterized by consistently accurate performance, and a "disengaged" state, marked by increased lapses. To better capture these latent strategic shifts, we propose employing Hidden Markov Models (HMMs). Our hypothesis is that modeling decision-making using HMMs will more accurately reflect experimental behavior compared to traditional models.

This methodological innovation is significant because it provides a more nuanced understanding of the behavioral policies governing perceptual decision-making. By explicitly modeling latent states, HMMs can reveal the hidden structure underlying perceptual errors, showing that lapses reflect deeper strategic changes rather than isolated occurrences.

Identifying and segmenting these latent strategies will open promising avenues for future research, including:

- Investigating the origins and adaptive functions of various decision-making strategies.

- Exploring the neural mechanisms underlying distinct behavioral states.

- Assessing whether these strategies represent bounded rationality or fluctuations in motivation.

![Proposed GM](HMM.png)
## Full project report: [GM_HMM.pdf](GM_HMM.pdf)

## References

1. **Ashwood, Z. C., Roy, N. A., Stone, I. R., International Brain Laboratory, Urai, A. E., Churchland, A. K., Pouget, A., & Pillow, J. W. (2022). Mice alternate between discrete strategies during perceptual decision-making.** *Nature Neuroscience*, 25(2), 201–212. Nature Publishing Group US New York.
2. **Bengio, Y., & Frasconi, P. (1994). An input output HMM architecture.** *Advances in Neural Information Processing Systems*, 7.
3. **International Brain Laboratory, Aguillon-Rodriguez, V., Angelaki, D., Bayer, H., Bonacchi, N., Carandini, M., Cazettes, F., Chapuis, G., Churchland, A. K., Dan, Y., & others. (2021). Standardized and reproducible measurement of decision-making in mice.** *eLife*, 10, e63711. eLife Sciences Publications, Ltd.
4. **Steckler, T. (2001). Using signal detection methods for analysis of operant performance in mice.** *Behavioural Brain Research*, 125(1–2), 237–248. Elsevier.
5. **Odoemene, O., Pisupati, S., Nguyen, H., & Churchland, A. K. (2018). Visual evidence accumulation guides decision-making in unrestrained mice.** *Journal of Neuroscience*, 38(47), 10143–10155. Society for Neuroscience.
6. **Luksys, G., Gerstner, W., & Sandi, C. (2009). Stress, genotype and norepinephrine in the prediction of mouse behavior using reinforcement learning.** *Nature Neuroscience*, 12(9), 1180–1186. Nature Publishing Group US New York.
7. **Bathellier, B., Tee, S. P., Hrovat, C., & Rumpel, S. (2013). A multiplicative reinforcement learning model capturing learning dynamics and interindividual variability in mice.** *Proceedings of the National Academy of Sciences*, 110(49), 19950–19955. National Academy of Sciences.
8. **Nowak, M., & Sigmund, K. (1993). A strategy of win-stay, lose-shift that outperforms tit-for-tat in the Prisoner's Dilemma game.** *Nature*, 364(6432), 56–58. Nature Publishing Group UK London.
