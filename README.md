# image-analysis-pipeline
End-to-end human image analysis pipeline using Python and AI – detect faces, emotions, posture, and clothing traits with annotated visual output.


Project Overview
----------------
Human Image Analysis Pipeline is an all-in-one, Python-based computer vision pipeline designed to extract meaningful human-centric attributes from images. This project combines state-of-the-art AI models to deliver demographic, emotional, visual, and posture-related insights — making it suitable for research, prototyping, and applied computer vision tasks.

Whether you're analyzing photos for a UX study, building a smart photo-tagging tool, or experimenting with multimodal image understanding, this notebook provides a fully modular and extensible foundation.

What This Notebook Does
------------------------
Given a user-uploaded image (e.g., a portrait or full-body photo), the pipeline performs:

- Face Detection & Analysis: Locates a face and estimates age and gender using `insightface`.
- Emotion Recognition: Uses `FER` to determine the dominant facial expression.
- Pose Estimation: Detects body landmarks via `MediaPipe`, including shoulders and hips, to infer posture and ensure valid region targeting.
- Clothing Color Detection: Extracts the upper-body clothing region and uses KMeans clustering to estimate dominant shirt color.
- Clothing Type Classification: Uses OpenAI's `CLIP` model to classify the type of clothing (e.g., jacket, t-shirt, sweater).
- Final Annotated Output: Combines all results in a summary and produces an annotated image with boxes and labels for easy visualization.

Why Use This Project
---------------------
- Combines multiple AI tools in a single, clean pipeline
- Requires no training — all models are pre-trained
- Extensible for research, CV portfolios, hackathons, or UX testing
- Easy to run in Google Colab or local Jupyter environments

Tools & Technologies Used
--------------------------
- OpenCV       : Image processing and drawing annotations
- InsightFace  : Face detection + age/gender estimation
- FER          : Emotion detection
- MediaPipe    : Body/face landmark detection & pose
- CLIP         : Multimodal text–image matching for clothing
- KMeans       : Shirt color clustering (OpenCV + scikit-learn)
