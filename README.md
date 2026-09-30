Our Approach: Inspired by Valdez-Valenzuela et al. (2025), who applied Text-GNN + GAT to detect AI-generated English text
Our contribution: We adapt and extend this framework to Arabic social media textReplace BERT/RoBERTa node features with AraBERT embeddings (Arabic-specific)
Apply to the ALHD Twitter/social media subset — short, noisy, dialectal Arabic
Add AraELECTRA and XLM-RoBERTa as transformer-based comparison points
Arabic LLM and Human Dataset (ALHD) Large-scale, multi-genre benchmark specifically designed for Arabic AI-generated text detection
 balanced 10% version, Twitter/social media subset

After preprocessing: 6,673 samples 50% human vs 50% machine generated text.

Directly mirrors real-world misinformation and fake content risks
Most detection work focuses on formal Arabic (news, reviews) — social media is underexplored

Split: Train 4,671 | Validation 1,003 | Test 999
Preprocessing :
Removed: URLs, mentions, hashtags, emojis, punctuation, non-Arabic characters
Discarded empty samples after cleaning
Why it matters: Short informal posts are extremely noisy; normalization reduces spurious variation
Visual: Before/after example of a tweet being cleaned


Models Overview:
8 models evaluated under the same train/val/test split:
Baseline: TF-IDF + Linear SVM
Transformers: AraBERT, AraELECTRA, XLM-RoBERTa
Graph-based: GCN (simple features), GAT (simple features), GCN + AraBERT, GAT + AraBERT
