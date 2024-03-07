Title: AlgoPuzzleVQA
Date: 2024-03-06
Category: Home

<div style="text-align: center;">
    <a href="https://arxiv.org/abs/2403.03864" class="button" style="margin: 0 10px;">Paper on ArXiv.org</a>
    <a href="https://github.com/declare-lab/puzzle-reasoning" class="button" style="margin: 0 10px;">Code on GitHub</a>
    <a href="https://github.com/declare-lab/puzzle-reasoning" class="button" style="margin: 0 10px;">HuggingFace Dataset</a>
</div>

### About

This paper introduces the novel task of multimodal puzzle solving, framed within the context of visual
question-answering. We present a new dataset, AlgoPuzzleVQA designed to challenge and evaluate the capabilities of
multimodal language models in solving algorithmic puzzles that necessitate both visual understanding, language
understanding, and complex algorithmic reasoning. We create the puzzles to encompass a diverse array of mathematical and
algorithmic topics such as boolean logic, combinatorics, graph theory, optimization, search, etc., aiming to evaluate
the gap between visual data interpretation and algorithmic problem-solving skills. The dataset is generated
automatically from code authored by humans. All our puzzles have exact solutions that can be found from the algorithm
without tedious human calculations. It ensures that our dataset can be scaled up arbitrarily in terms of reasoning
complexity and dataset size. Our investigation reveals that large language models (LLMs) such as GPT4V and Gemini
exhibit limited performance in puzzle-solving tasks. We find that their performance is near random in a multi-choice
question-answering setup for a significant number of puzzles. The findings emphasize the challenges of integrating
visual, language, and algorithmic knowledge for solving complex reasoning problems.

### Puzzle Ontology

Our puzzles encompass a diverse range of visual, mathematical and algorithmic topics. We categorize the visual and
algorithmic features present in each puzzle in the image below:

![](/images/categories.png)

### Dataset

Our current version of AlgoPuzzleVQA contains problems with easy to moderate difficulty, many of which can be solved by
humans by hand without applying the underlying algorithm. Our puzzles encompass a diverse range of visual, mathematical,
and algorithmic topics. In total, we have 1800 instances from the 18 different puzzles following various feature
combinations from our ontology. We consider the full dataset as an evaluation-only benchmark.
Many of these puzzles are popular in various recreational or academic settings. The image below shows examples of
puzzles from our dataset based on algorithmic features:

![](/images/examples.png)

We also show examples of puzzles based on visual features below. We show one instance of a puzzle from each of the four
visual
categories. Note that the header categories are not exhaustive as some puzzles may belong to more visual categories than
the ones shown in the header.

![](/images/features.png)

### Example Puzzle

The image below shows an example of the Color Hue puzzle in our dataset:

![](/images/color_hue.png)

Question: A 5 * 4 board consists of
20 different coloured tiles. A random state the board is shown in (A). The ideal state of the board is shown in (B). A
swap consists of selecting any two tiles in the board and switching their positions. What is the minimum number of swaps
required to restore the ideal state of the board from (A)? Gold Answer: 4

### Evaluation Results

Our main evaluation results are shown below. The Board Tiling puzzle has a random baseline performance of 50%. All other
puzzles have a random baseline
performance of 25%. The overall random baseline stands at 26.4%. We notice that the performance in a significant
number of these puzzles across all the models is close to the random baseline of 50% and 25%. The GPT-4V model in the
eCoT setup achieves the best score overall with an average accuracy of 31.6%, which is only around 5% better than
random. The other models perform poorer, with Gemini Pro obtaining a best of 29.5%, Instruct-BLIP obtaining a best of
29.1% with the 7B model, and LLaVA obtaining 29.1%.

![](/images/results.png)

### Citation

If our work inspires your research, please cite us:

```
@article{ghosal2024algopuzzlevqa,
  title={Are Language Models Puzzle Prodigies? Algorithmic Puzzles Unveil Serious Challenges in Multimodal Reasoning},
  author={Ghosal, Deepanway and Han, Vernon Toh Yan and Chia, Yew Ken and and Poria, Soujanya},
  journal={arXiv preprint arXiv:2403.03864},
  year={2024}
}
```

### Contact

For any questions, please open an issue on [GitHub](https://github.com/declare-lab/puzzle-reasoning/issues).

<br>
<a href="https://declare-lab.github.io">
    <img src="https://declare-lab.github.io/assets/images/logos/square-light.png" alt="Declare Lab Logo" style="width: 200px; height: auto;">
</a>
