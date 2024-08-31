# Mental-Health-Support-Mobile-Application
## Overview
Mental-Health-Support-Mobile-Application is an innovative mobile app designed to provide mental health support through an AI-powered chatbot that acts as a virtual therapist. It also includes web scraping features for social media analysis to detect signs of mental health distress and an emergency system for users at risk of suicide.

The application leverages advanced technologies like Natural Language Processing (NLP), Neural Networks, and Flutter to deliver a comprehensive mental health support tool.
### Phase 1: Mood Tracking
This repository contains the code for the Mood Tracking component, the first phase of the development process. This component uses a fine-tuned transformer model to classify emotions in text data, allowing the AI-powered chatbot to assess the user’s emotional state.
#### Model and Datasets
- Pretrained Model: The mood tracking model is based on the [roberta-base-go_emotions](https://huggingface.co/SamLowe/roberta-base-go_emotions) transformer model, pretrained on the GoEmotions dataset from Hugging Face.
- Fine-Tuning:
  - The model was first fine-tuned using the [SetFit/emotion](https://huggingface.co/datasets/SetFit/emotion) dataset from Hugging Face.
  - A second fine-tuning was performed using the [Emotion Detection from Text dataset](https://www.kaggle.com/datasets/pashupatigupta/emotion-detection-from-text) from Kaggle.
Getting Started
Prerequisites
To run the code, you need the following:
- Python 3.8 or later
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- Scikit-Learn
- Pandas
Install the required Python libraries using:
```bash
pip install torch transformers datasets scikit-learn pandas
```
Usage
1. Clone the Repository
```bash
git clone https://github.com/maryamesh/Mental-Health-Support-Mobile-Application.git
cd Mental-Health-Support-Mobile-Application
```
2. Run the Mood Tracking Script
The script `mood_tracking.py` processes the input text data and evaluates the user's mood:
```bash
python mood_tracking.py
```
Ensure that you have the dataset `tweet_emotions.csv` in the correct path, or adjust the file path in the script accordingly.
Code Explanation
- **Loading Pretrained Model**: The script begins by loading a pretrained transformer model from Hugging Face (`roberta-base-go_emotions`) and fine-tunes it on custom datasets to adapt it to the mood tracking use case.
- **Preprocessing**: Text data is preprocessed to remove unnecessary columns (`tweet_id`, `sentiment`) and is tokenized using the Hugging Face tokenizer for input to the model.
- **Model Evaluation**: The fine-tuned model predicts the user's emotional state based on their text input. The script outputs the predicted probabilities for each emotion label.
Future Development
- **Phase 2**: Integrate the mood tracking model with the AI-powered chatbot for real-time emotion detection and response generation.
- **Phase 3**: Implement web scraping features for social media analysis to identify signs of mental health distress.
- **Phase 4**: Develop an emergency response system for users at risk of suicide, including features for alerting emergency contacts or hotlines.
Technologies Used
- **Natural Language Processing (NLP)**: For understanding and classifying user emotions.
- **Neural Networks**: To power the AI-driven chatbot and emotion detection models.
- **Flutter**: For building the mobile application across multiple platforms.

## Contributing
Contributions are welcome! Feel free to submit a pull request or open an issue if you have suggestions, bug reports, or feature requests.
Contact
For questions or suggestions, please contact [Maryam Eslam Elhossary](mailto:maryamesh1911@gmail.com).


MIT License

Copyright (c) 2024 [Maryam Eslam]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

### Acknowledgments

This project makes use of the following open-source datasets and models:

1. **[SetFit/emotion dataset](https://huggingface.co/datasets/SetFit/emotion)**
   - Used for fine-tuning the model. Please review the dataset's page for specific licensing terms.
   - Credits to the dataset creators.

2. **[roberta-base-go_emotions model](https://huggingface.co/SamLowe/roberta-base-go_emotions)**
   - A pretrained transformer model used as the base model in this project. Please review the model's page for specific licensing terms.
   - Credits to Sam Lowe and Hugging Face.

3. **[Emotion Detection from Text dataset](https://www.kaggle.com/datasets/pashupatigupta/emotion-detection-from-text)**
   - Used for further fine-tuning the model. Please review the dataset's page for specific licensing terms.
   - Credits to the dataset creator, Pashupati Gupta.

Please ensure compliance with the respective licenses for the datasets and models used in this project. Any use of these datasets and models is subject to the terms and conditions specified by their respective owners.


