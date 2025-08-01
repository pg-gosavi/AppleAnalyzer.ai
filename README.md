Here’s a professional and informative `README.md` for your **AppleAnalyzer AI** project:

---

# 🍏 AppleAnalyzer AI

AppleAnalyzer AI is an intelligent, end-to-end apple freshness detection system powered by **YOLOv8**, **ResNet18**, and **Groq LLaMA 3**. This agentic pipeline detects apples from uploaded images, classifies them as **Fresh** or **Rotten**, and provides insightful suggestions from a simulated AI agricultural expert.

## ✨ Features

* 🍎 **Apple Detection**: Uses YOLOv8 for precise apple localization.
* 🧠 **Freshness Classification**: Classifies each detected apple using ResNet18 (Fresh/Rotten).
* 💬 **AI Feedback**: Groq-hosted LLaMA 3 provides human-readable advice and summaries.
* 🤖 **Agentic Workflow**: Built with LangGraph to maintain state, memory, and logical progression.
* 📷 **Gradio Interface**: User-friendly web interface for interaction and testing.

---

## 🔧 Tech Stack

| Component      | Tech Used                          |
| -------------- | ---------------------------------- |
| Detection      | YOLOv8                             |
| Classification | ResNet18 (custom fine-tuned model) |
| Reasoning      | LLaMA 3 hosted via Groq API        |
| Orchestration  | LangGraph + LangChain              |
| UI             | Gradio                             |
| Others         | OpenCV, Torch, PIL, NumPy          |

---

## 🚀 Setup Instructions

1. **Clone the Repository**

```bash
git clone https://github.com/your-username/appleanalyzer-ai.git
cd appleanalyzer-ai
```

2. **Install Requirements**

```bash
pip install torch torchvision ultralytics gradio pillow groq langgraph langchain opencv-python
```

3. **Add Groq API Key**

```bash
export GROQ_API_KEY="your_groq_api_key"
```

4. **Model Setup**

* Place your **YOLOv8 model** at:

  ```
  /content/drive/MyDrive/detection_type/apple_detection/rotten_model/best.pt
  ```

* Place your **ResNet18 model weights** at:

  ```
  /content/drive/MyDrive/improved_apple_classifier_resnet18.pth
  ```

> Update paths in the script if needed for local runs.

5. **Run the App**

```bash
python appleanalyzer_ai.py
```

The Gradio interface will open in your browser.

---

## 🧠 Agent Workflow

1. **Image Upload**
2. **YOLOv8** detects all apples in the image
3. **ResNet18** classifies each detected apple
4. **Groq LLaMA 3** summarizes the result and gives expert recommendations
5. **LangGraph** maintains memory of previous predictions for adaptive reasoning

---

## 📷 Sample Output

* Bounding boxes colored green (Fresh) or red (Rotten)
* Confidence score shown
* AI-generated suggestion about the detected apples

---

## 📁 Directory Structure

```
.
├── appleanalyzer_ai.py
├── models/
│   ├── best.pt
│   └── improved_apple_classifier_resnet18.pth
├── retrain/
│   └── Fresh/ or Rotten/  # Uncertain samples saved here
```

---

## 📌 Future Improvements

* Add **multi-fruit detection** (banana, mango, etc.)
* Use **active learning** from uncertain predictions
* Integrate with **cloud storage** and APIs

---

## 🧑‍🌾 Use Case

This project is ideal for:

* Farmers and distributors checking produce quality
* Smart agriculture AI systems
* AI-powered food inspection

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙌 Acknowledgments

* [YOLO by Ultralytics](https://github.com/ultralytics/ultralytics)
* [ResNet](https://arxiv.org/abs/1512.03385)
* [Groq LLaMA 3](https://groq.com/)
* [Gradio](https://gradio.app/)
* [LangGraph](https://docs.langchain.com/langgraph/)


