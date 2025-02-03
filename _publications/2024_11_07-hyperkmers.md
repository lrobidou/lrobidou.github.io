---
title: "Hyper-k-mers: efficient streaming k-mers representation"
collection: publications
permalink: /publication/2024_11_07-hyperkmers
# excerpt: ''
date: 2024_11_07
venue: 'Preprint'
paperurl: 'https://www.biorxiv.org/content/10.1101/2024.11.06.620789v1'
# citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
Igor Martayan\*, Lucas Robidou\*, Yoshihiro Shibuya, Antoine Limasset<br/>\* co-first authors

K-mers have become ubiquitous in modern bioinformatics pipelines. A key factor in their success is the ability to filter out erroneous k-mers by removing those with low abundances. However, large numbers of distinct k-mers make counting a memory-intensive step. Early tools addressed this issue by storing k-mers on disk. More recent solutions, mitigate the excessive redundancy of overlapping k-mers by partially reassembling them into super-k-mers. Nevertheless, consecutive super-k-mers still overlap by k−1 bases, leading to some degree of inefficiency.

Here we present hyper-k-mers as an alternative, less redundant, representation of super-k-mers. Our contributions are three-fold. First, we propose hyper-k-mers, a new k-mer representation that asymptotically decreases duplication compared to super-k-mers. Second, we present a theoretical analysis comparing the space efficiency of super-k-mers, syncmers, and hyper-k-mers. Our approach offers significant advantages compared to super-k-mers, by reducing the asymptotic lower bound from 6 to 4 bits per nucleotide. Third, we present KFC, a k-mer counting algorithm leveraging hyper-k-mers. KFC offers significant practical advantages, including an order of magnitude improvement in memory usage compared to state-of-the-art tools. Notably, our experiments show that KFC is the only tool whose memory usage scales sub-linearly with k-mer size k, and is the fastest option when k is large.

KFC is available at https://github.com/lrobidou/KFC with tests available at https://github.com/imartayan/KFC_experiments

[Download paper here](https://academic.oup.com/bioinformatics/article/39/5/btad305/7169157)