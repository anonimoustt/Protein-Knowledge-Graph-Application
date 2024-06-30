# Protein-Knowledge-Graph-Application

In this research, we have shown that the efficient incorporation of the Protein Knowledge Graph cant detect the scientifically importannt relations among the full protein sequences. 

# Data

We have leveraged  ProteinKG25 ( https://www.zjukg.org/project/ProteinKG25/ ) knowledge graph data, and phosphosites curated data (https://huggingface.co/datasets/waylandy/phosformer_curated/blob/main/curated/phosphosites_11mer_kinase_specific.tsv). We have also leveraged the following databases:

Reactome Database: https://drive.google.com/file/d/1k1NuOmRCrFNp0S4EyRmfXVjwJTZI8pzN/view?usp=sharing

Phosphorylation Databse: https://drive.google.com/file/d/1hjUg_jFUhuhrBN3hw4H5y4mJYgv08ew6/view?usp=sharing

ProteinKG25 knowledge graph can be accessed from the following google drive link: 

https://drive.google.com/drive/folders/1UzEb-mWO6gG2GyQqmQG_oF8vWqmKkDfG?usp=sharing

# Data from our Expermental Outcomes ( The data is used in Global Ranking )

Protein Sequence Pairs ( that appear together only after incorporating knowledge graph ) using TransE embedding model: https://drive.google.com/file/d/1x3e6q4AQB6QepVkta751RnjLHd764Uyt/view?usp=sharing

Protein Sequence Pairs ( that appear together only after incorporating knowledge graph ) using RotatE embedding model: https://drive.google.com/file/d/1TUcfOlAqmeWDzZi6_z_2GiHFxaynFZuW/view?usp=sharing


Protein Sequence Pairs ( that appear together only after incorporating knowledge graph ) using HolE embedding model: 
https://drive.google.com/file/d/1GWUpJXVZAT1HUX9siEyOm9PCk6An8mBR/view?usp=sharing

Protein Sequence Pairs ( that appear together only after incorporating knowledge graph ) using DistMult embedding model: 
https://drive.google.com/file/d/19GCax77Ue8RAl8OjUO1F2qxivO4RSz5i/view?usp=sharing

Protein Sequence Pairs ( that appear together only after incorporating knowledge graph ) using ComplEx embedding model: 
https://drive.google.com/file/d/18N6Qbt7P_98KisOT_boJndNKsQjdwOYn/view?usp=sharing

# Code
 The code to generate the outcomes incorporating knowledge graph can be accessed in ProteinKg25_ESM-2_Application notbook. In ProteinKg25_ESM-2_Application notebook,
 to have results for the different embedding models, in cell named " Ampligraph Library to extract the knowledge graph embedding", the following code editing is required:

 modeluu = ScoringBasedEmbeddingModel(k=320, eta=1, scoring_type='HolE')

 In the above line of modeluu replce scoring_type with the target embedding model names. We have leveraged 5 embedding models. 
 5 embedding models are: ['HolE', 'RotatE', 'ComplEx', 'DistMult', 'TransE']

 The code of Global ranking can be accessed through the following google colab link:
 
 https://colab.research.google.com/drive/1wo-Zdb8rgeD7RJvY4XKo7xpjdDjeXFHr?usp=sharing















