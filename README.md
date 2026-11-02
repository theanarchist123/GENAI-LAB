# BattingCoach — Generative AI Experiments (1–11)

This folder contains one Jupyter notebook for each experiment in the supplied ZIP.

## Important dataset mapping

The GitHub project is **BatCoach AI Pro**, not a single general-purpose dataset. The repository documents:

1. **Cricket Bat detection dataset** — Roboflow Cricket Bat Dataset, 930 images, one class (`Bat`), YOLOv8 Oriented Bounding Box annotation format. `README.dataset.txt`, `README.roboflow.txt`, and `data.yaml` document it.
2. **Cricket shot classification dataset** — project code refers to `rokmr/cricketshot`, with ten shot classes: `cover`, `defense`, `flick`, `hook`, `late_cut`, `lofted`, `pull`, `square_cut`, `straight`, `sweep`. The backend also references a fine-tuned VideoMAE checkpoint on Hugging Face.
3. **Project knowledge/documentation** — README, code descriptions, and wiki describe MediaPipe biomechanics, YOLOv8-OBB bat detection, VideoMAE shot classification, practice modes, and system architecture.

The notebooks use these sources for project-domain NLP, prompt engineering, semantic retrieval, RAG, and Responsible AI tests. Experiments 4 and 6 use MNIST because their handouts explicitly prescribe handwritten digits for VAE/GAN. Experiment 5 uses English/French reference translations because its handout explicitly prescribes T5 translation. It would be methodologically incorrect to claim those unrelated tasks were trained on the cricket-bat detection images.

## Running the notebooks

- Recommended: Google Colab (GPU useful for VAE/GAN and model inference).
- Open each `.ipynb` and execute cells from top to bottom.
- Install cells use `%pip`; internet is required for package/model downloads.
- Hugging Face model downloads can be slow and may require account access for gated models.
- Some models may be slow on CPU. Use GPU runtime where available.
- Notebooks do not require API keys. Never paste personal or secret credentials into a notebook.
- RAG and semantic retrieval use a small documented project-domain text corpus. Inspect all retrieved chunks and fill the relevance/evaluation tables based on actual output.

## Notebook index

| Experiment | Notebook | Main activity |
|---|---|---|
| 1 | `Experiment_1_Getting_Started.ipynb` | Python environment + pre-trained text generation |
| 2 | `Experiment_2_Text_Preprocessing.ipynb` | NLP preprocessing, tokenization, Word2Vec and sentence embeddings |
| 3 | `Experiment_3_Prompt_Engineering.ipynb` | Zero-shot, few-shot, structured reasoning and role prompts |
| 4 | `Experiment_4_VAE.ipynb` | MNIST VAE reconstruction, generation and latent visualization |
| 5 | `Experiment_5_Translation_Visualization.ipynb` | T5 English→French, BLEU, six plots |
| 6 | `Experiment_6_GAN.ipynb` | MNIST GAN training and synthetic images |
| 7 | `Experiment_7_GPT_BERT_Comparison.ipynb` | GPT generation vs BERT understanding |
| 8 | `Experiment_8_Semantic_Search.ipynb` | Sentence embeddings + FAISS semantic retrieval |
| 9 | `Experiment_9_RAG_Document_QA.ipynb` | Project documentation RAG with source labels |
| 10 | `Experiment_10_Responsible_AI_Evaluation.ipynb` | BLEU, ROUGE, perplexity, bias, hallucination, privacy and ethics |
| 11 | `Experiment_11_Gradio_GenAI_App.ipynb` | Interactive Gradio app with validation and controls |

## Submission notes

Outputs in the notebooks are generated only when you run them. The notebooks are not pre-populated with fabricated training results. Add screenshots, actual outputs, observations, and your own conclusions after execution. For experiment 10, fixed candidate texts are explicitly labelled as illustrative evaluation inputs; replace them with actual model outputs if your instructor expects generated candidates.
