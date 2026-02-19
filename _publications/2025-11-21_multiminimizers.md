---
title: "Minimizer Density revisited: Models and Multiminimizers"
collection: publications
permalink: /publication/2025-11-21_multiminimizers
# excerpt: ''
date: 2024_11_07
venue: 'Preprint'
paperurl: 'https://www.biorxiv.org/content/10.1101/2024.11.06.620789v1'
# citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
Florian Ingels, Lucas Robidou, Igor Martayan, Camille Marchet, Antoine Limasset

High-throughput sequence analysis commonly relies on k-mers (words of fixed length k) to remain tractable at modern scales. These k-mer-based pipelines can employ a sampling step, which in turn allows grouping consecutive k-mers into larger strings to improve data locality. Although other sampling strategies exist, local schemes have become standard: such schemes map each k-mer to the position of one of its characters. A key performance measure of these schemes is their density, defined as the expected fraction of selected positions. The most widely used local scheme is the minimizer scheme: given an integer m ≤ k, a minimizer scheme associates each k-mer to the starting position of one of its m-mers, called its minimizer. Being a local scheme, the minimizer scheme guarantees covering all k-mers of a sequence, with a maximal gap between selected positions of w = k − m + 1. Recent works have established near-tight lower bounds on achievable density under standard assumptions for local schemes, and state-of-the-art schemes now operate close to these limits, suggesting that further improvements under the classical notion of density will face diminishing returns. Hence, in this work, we aim to revisit the notion of density and broaden its scope.

As a first contribution, we draw a link between density and the gap between consecutive selected positions. We propose a probabilistic model allowing us to establish that the density of a local scheme is exactly the inverse of the expected gap between the positions it selects, under the minimal and only assumption that said gaps are somehow equally distributed. We emphasize here that our model makes no assumptions about how positions are selected, unlike the classical models in the literature. Our result introduces a novel method for computing the density of a local scheme, extending beyond classical settings.

Based on this analysis, we introduce a novel technique, named multiminizers, by associating each k-mer with a bounded set of candidate minimizers rather than a single one. The candidate furthest away (in a precise sense defined in the article) is selected. Since the decision is made by taking advantage of a context beyond a single k-mer, this technique is not a local scheme — as a result, we propose the concept of semi-local schemes, which provide a broader framework within which our method fits. Using the multiminimizer trick on a local scheme reduces its density at the expense of a controlled increase in computation time. We show that this method, when applied to random (hash-based) minimizers and to open-closed mod-minimizers, achieves asymptotically optimal density, representing, to our knowledge, the first construction converging to this limit.

Our third contribution is the introduction of the deduplicated density, which measures the fraction of distinct minimizers used to cover all k-mers of a set of sequences. While this problem has gained traction in applications such as assembly, filtering, and pattern matching, standard minimizer schemes are often used as a proxy, blurring the distinction between the two objectives (minimizing the number of selected positions or the number of selected minimizers). Although related to the classical notion of density, deduplicated density differs in both definition and suitable constructions, and must be analyzed in its own right, together with its precise connections to standard density. We show that multiminimizers can also improve this metric, but that globally minimizing deduplicated density in this setting is NP-complete, and we instead propose a local heuristic with strong empirical behavior.

Finally, we show that multiminimizers can be computed efficiently, and provide a SIMD-accelerated Rust implementation together with proofs of concept demonstrating reduced memory footprints on core sequence-analysis tasks. We conclude with open theoretical and practical questions that remain to be addressed in the area of density.

Our minimizer iterator is available at https://github.com/lrobidou/multiminimizers .

[Download paper here](https://www.biorxiv.org/content/10.1101/2025.11.21.689688v2)