TD RNA-seq – Analyse Différentielle et Enrichissement Fonctionnel  
## TCGA-COAD (Colon Adenocarcinoma)

**Université de Lille**  
Responsable : *Yanis Zirem*  
Niveau : Master / Bioinformatique / Biologie computationnelle  

---

#  Contexte scientifique

Ce TD repose sur les données publiques du projet **TCGA-COAD (The Cancer Genome Atlas – Colon Adenocarcinoma)**.

Le projet TCGA (2006–2018) constitue le plus grand effort international de caractérisation moléculaire des cancers :

- 33 types de cancer
- > 11 000 patients
- Approche multi-omics (WGS, RNA-seq, CNV, méthylation, protéomique)
- Données open-access (GDC Portal)

Publication de référence :

> The Cancer Genome Atlas Network.  
> Comprehensive molecular characterization of human colon and rectal cancer.  
> *Nature* 487, 330–337 (2012).  
> DOI: 10.1038/nature11252

---

#  Dataset utilisé dans ce TD

- **Projet** : TCGA-COAD  
- **Technologie** : RNA-seq (Illumina HiSeq 2000/2500)  
- **Alignement** : STAR v2.7  
- **Quantification** : HTSeq-Counts  
- **Échantillons utilisés** :
  - Primary Solid Tumor
  - Solid Tissue Normal  
- ~60 000 features (≈ 20 000 gènes codants)

Le dataset fourni dans ce dépôt correspond à un sous-ensemble filtré et pré-traité à des fins pédagogiques.

---

#  Objectifs pédagogiques

À la fin de ce TD, les étudiants seront capables de :

##  Compétences techniques

1. Charger et inspecter des données RNA-seq réelles (TCGA-COAD)
2. Réaliser un **contrôle qualité complet** :
   - Boxplots, density plots, violin plots
   - PCA (PC1/PC2, scree plot)
   - Clustering hiérarchique
   - Heatmap des distances
3. Effectuer une **analyse différentielle avec DESeq2** :
   - Normalisation
   - Estimation des dispersions
   - Test de Wald
   - Extraction des gènes significatifs (padj, log2FC)
4. Générer des visualisations professionnelles :
   - MA plot
   - Volcano plot
   - Heatmaps hiérarchiques
   - Count plots de gènes individuels
5. Interpréter les statistiques :
   - p-value
   - FDR (padj)
   - log2 Fold Change
   - baseMean
6. Réaliser des **analyses d’enrichissement fonctionnel** :
   - GO Biological Process (ORA)
   - KEGG Pathways (ORA)
   - GSEA sur KEGG (NES, running score)
   - Reactome Pathways
7. Comparer **ORA vs GSEA** (principes, interprétation du NES)

---

##  Compétences biologiques

Les étudiants devront :

- Interpréter les résultats dans le contexte du **cancer colorectal (CRC)**
- Identifier les voies dérégulées (Wnt, MAPK, PI3K/Akt, cycle cellulaire)
- Proposer des gènes candidats pour validation expérimentale

---
