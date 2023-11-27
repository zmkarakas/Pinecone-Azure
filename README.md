# Pinecone-Azure

### Problem statement
At the time of writing, Assistants ("Retrieval") on OpenAI have these limits: 

1. You can attach a maximum of 20 files per Assistant, and they can be at most 512 MB each. 

2. The size of all the files uploaded by your organization should not exceed 100GB (although this is upgradable).

On top of this, there might be restrictions not specified in the documentation.  Therefore, there needs to be solution to the limits of the CustomGPT or Assistant knowledge base required for enterprise and larger data setups and scenarios. Enterprises currently have more than hundreds or thousands (or more) of files and TBs or PBs of data (which need to be vectorized to be accessed by the GPT). In order to alleviate the problem, I came up with a setup using a vectorDB such as Pinecone, which is a managed solution. Other vectorDBs such as Chroma can also be used. 

### Diagram of Architecture

For this project I will be using OpenPowerlifting's full dataset (dated 2023-11-25) available here: https://openpowerlifting.gitlab.io/opl-csv/bulk-csv.html
Unzipped size is around 550MBs, and a single CSV file. Also note that this dataset is updated daily. The dataset slightly exceeds the limit of 512 MB.

![Miroboard](https://github.com/zmkarakas/Pinecone-Azure/assets/50174304/850fa03b-c64e-4746-aef9-1e1008d66594)


