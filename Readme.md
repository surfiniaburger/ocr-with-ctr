#### ## Inspiration
> "While modern VLMs are masters of English and Chinese, they often treat Right-to-Left (RTL) scripts like Arabic and Persian as an afterthought. We built **Glimpse** to prove that the **PaddleOCR-VL** architecture can be 'globalized' through specialized fine-tuning, bringing high-precision OCR to under-represented, low-resource languages."

#### ## Challenges we ran into
> "The primary hurdle was **'Script Bias.'** Base models are pre-trained on Left-to-Right (LTR) data. When presented with Arabic/Persian, the model's visual grounding and sequential logic were initially misaligned (Base CER: ~58%). We had to implement a training regime that focused on **Unicode-aware alignment** to handle the complex ligatures and cursive nature of the RTL script."

#### ## Accomplishments that we're proud of
> "We successfully reduced the Character Error Rate (CER) from a chaotic baseline to an industrial-grade **6.9%** in just 500 steps. We achieved a near-perfect validation loss of **0.25**, demonstrating that Glimpse has successfully mastered the linguistic 'joiner' logic of the Arabic script, producing human-legible transcriptions from diverse visual fonts."

#### ## What we learned
> "We learned that even a model with a billion parameters needs 'linguistic discipline.' Fine-tuning isn't just about showing more images; it’s about aligning the model's internal probability map to the specific grammar of the target language. In the RTL domain, **Inference Normalization** is just as important as training loss."

#### ## Credit & Aknowledgement
> **Data Acknowledgements:**
> We would like to express our gratitude to **Mohammad Javad Esmaeili** for providing the `Persian_Arabic_TextLine_Image_Ocr_Medium` dataset. This open-source contribution was essential in training our model to handle the nuances of Persian and Arabic scripts.
