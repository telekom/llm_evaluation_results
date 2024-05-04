# LLM Evaluation Results

This project collects and visualizes our LLM evaluation results.

## German RAG LLM Evaluation

The German LLM evaluation is based on the
[german_rag_eval](https://huggingface.co/datasets/deutsche-telekom/Ger-RAG-eval) dataset.

| model name                                               |   choose context by question acc |   choose question by context acc |   context question match acc |   question answer match acc |   all acc |   all acc stderr |
|:---------------------------------------------------------|---------------------------------:|---------------------------------:|-----------------------------:|----------------------------:|----------:|-----------------:|
| VAGOsolutions/Llama-3-SauerkrautLM-70b-Instruct          |                            0.998 |                            1     |                        0.973 |                       0.949 |   0.98    |       0.0033755  |
| VAGOsolutions/SauerkrautLM-Mixtral-8x7B-Instruct         |                            0.953 |                            0.998 |                        0.975 |                       0.974 |   0.975   |       0.00452096 |
| mistralai/Mixtral-8x7B-Instruct-v0.1                     |                            0.94  |                            0.998 |                        0.973 |                       0.973 |   0.971   |       0.00479586 |
| meta-llama/Meta-Llama-3-70B-Instruct                     |                            0.94  |                            1     |                        0.974 |                       0.946 |   0.965   |       0.00492486 |
| microsoft/Phi-3-mini-4k-instruct                         |                            0.847 |                            0.998 |                        0.965 |                       0.964 |   0.9435  |       0.00612787 |
| VAGOsolutions/Llama-3-SauerkrautLM-8b-Instruct           |                            0.928 |                            0.824 |                        0.982 |                       0.906 |   0.91    |       0.00841656 |
| meta-llama/Meta-Llama-3-8B-Instruct                      |                            0.725 |                            0.855 |                        0.977 |                       0.943 |   0.875   |       0.00933624 |
| DiscoResearch/DiscoLM_German_7b_v1                       |                            0.625 |                            0.991 |                        0.914 |                       0.927 |   0.86425 |       0.0088514  |
| occiglot/occiglot-7b-de-en-instruct                      |                            0.343 |                            0.994 |                        0.863 |                       0.969 |   0.79225 |       0.00845623 |
| occiglot/occiglot-7b-eu5-instruct                        |                            0.722 |                            0.982 |                        0.587 |                       0.814 |   0.77625 |       0.0115674  |
| LeoLM/leo-mistral-hessianai-7b-chat                      |                            0.865 |                            0.949 |                        0.735 |                       0.52  |   0.76725 |       0.0118855  |
| occiglot/occiglot-7b-de-en                               |                            0.453 |                            0.698 |                        0.501 |                       0.5   |   0.538   |       0.0154785  |
| DiscoResearch/Llama3_DiscoLM_German_8b_v0.1_experimental |                            0.303 |                            0.28  |                        0.751 |                       0.594 |   0.482   |       0.0144911  |
| occiglot/occiglot-7b-eu5                                 |                            0.327 |                            0.582 |                        0.5   |                       0.5   |   0.47725 |       0.0155215  |

- results can be found in this notebook: [german_rag_eval.ipynb](german_rag_eval.ipynb)
- raw data can be found in this folder: [german_rag_eval](german_rag_eval)
- The evaluation was carried out with [LightEval](https://github.com/huggingface/lighteval) and
the `--use_chat_template --override_batch_size 1` options.

## Open LLM Leaderboard Evaluation

The open LLM leaderboard evaluation.

| model name                               |   arc acc |   arc acc stderr |   arc acc norm |   arc acc norm stderr |   hellaswag acc |   hellaswag acc stderr |   hellaswag acc norm |   hellaswag acc norm stderr |   truthfulqa truthfulqa mc1 |   truthfulqa truthfulqa mc1 stderr |   truthfulqa truthfulqa mc2 |   truthfulqa truthfulqa mc2 stderr |   winogrande acc |   winogrande acc stderr |   gsm8k qem |   gsm8k qem stderr |   mmlu acc |   mmlu acc stderr |   all acc |   all acc stderr |   all acc norm |   all acc norm stderr |   all truthfulqa mc1 |   all truthfulqa mc1 stderr |   all truthfulqa mc2 |   all truthfulqa mc2 stderr |   all qem |   all qem stderr |
|:-----------------------------------------|----------:|-----------------:|---------------:|----------------------:|----------------:|-----------------------:|---------------------:|----------------------------:|----------------------------:|-----------------------------------:|----------------------------:|-----------------------------------:|-----------------:|------------------------:|------------:|-------------------:|-----------:|------------------:|----------:|-----------------:|---------------:|----------------------:|---------------------:|----------------------------:|---------------------:|----------------------------:|----------:|-----------------:|
| microsoft/Phi-3-mini-4k-instruct         |  0.620307 |        0.0141821 |       0.656997 |             0.0138724 |        0.610635 |             0.0048661  |             0.787791 |                  0.00408036 |                    0.440636 |                          0.0173797 |                    0.626144 |                          0.015784  |         0.716654 |               0.0126648 |    0.636088 |          0.0132525 |   0.686758 |         0.0326675 |  0.68488  |        0.0315626 |       0.722394 |            0.00897639 |             0.440636 |                   0.0173797 |             0.626144 |                   0.015784  |  0.636088 |        0.0132525 |
| vonjack/Phi-3-mini-4k-instruct-LLaMAfied |  0.616894 |        0.0142065 |       0.645904 |             0.0139755 |        0.609241 |             0.00486923 |             0.789385 |                  0.00406912 |                    0.462668 |                          0.0174546 |                    0.63262  |                          0.0158538 |         0.724546 |               0.0125557 |    0.63533  |          0.0132584 |   0.669958 |         0.0328833 |  0.668972 |        0.0317663 |       0.717645 |            0.00902229 |             0.462668 |                   0.0174546 |             0.63262  |                   0.0158538 |  0.63533  |        0.0132584 |

- results can be found in this notebook: [open_llm_leaderboard_eval.ipynb](open_llm_leaderboard_eval.ipynb)
- raw data can be found in this folder: [open_llm_leaderboard](open_llm_leaderboard)
- The evaluation was carried out with [LightEval](https://github.com/huggingface/lighteval) and
the `--use_chat_template --override_batch_size 1` options.

## Licensing

Copyright (c) 2024 [Philip May](https://philipmay.org), [Deutsche Telekom AG](https://www.telekom.de/)\
Copyright (c) 2024 [Philip May](https://philipmay.org)

Licensed under the **MIT License** (the "License"); you may not use this file except in compliance with the License.
You may obtain a copy of the License by reviewing the file
[LICENSE](https://github.com/telekom/llm_evaluation_results/blob/main/LICENSE) in the repository.
