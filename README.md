Project Description
This project uses Google’s Teachable Machine to train an image classification model that recognizes common desk objects using a webcam. The trained model is exported as TensorFlow.js files and uploaded to GitHub along with a reflection on its performance.
## Classes Identified
The model was trained to identify the following five desk objects:

Class 1: Pencils

Class 2: Pens

Class 3: Electric Pencil Sharpener

Class 4: Keyboard

Class 5: Mouse

## Discussion & Reflection

1.  **Model Performance & Iteration:**
    * How accurate was your first trained model?
    My first trained model showed mixed accuracy: it performed extremely well on large, high‑contrast objects like the keyboard and pencil sharpener, but struggled heavily with thin objects such as pens and pencils.
    * What steps did you take to iterate and improve its performance? (e.g., added more images, diversified image types for a specific class).
    To improve performance, I added more images for the weaker classes and captured them at different angles, distances, and backgrounds
    * How did these changes affect the model's accuracy and confidence scores?
    These changes helped slightly, but the confidence scores for pens and pencils still remained low (around 12–25%), showing that some objects are inherently harder for the model to learn due to shape and contrast limitations.

2.  **Challenges & Observations:**
    * Which objects were the easiest for your model to learn and distinguish? Why do you think that was?
    The easiest objects for the model to learn were the keyboard and the electric pencil sharpener because they are large, have distinct shapes, and contain strong visual features that stand out to the webcam. 
    
    * Which objects were the most challenging? What made them difficult (e.g., similar shapes, variable appearances)?
    The most challenging objects were pens and pencils, which are thin, visually similar, and often blend into the background, making them difficult for the model to distinguish.
    
    * What happened when you showed the model an object it wasn't trained on? How did the confidence scores behave, and why is this significant?
    When I showed the model an object it wasn’t trained on, it produced low‑confidence guesses and tried to match it to the closest-looking class, which shows how the model relies on pattern similarity rather than true understanding.

3.  **Bias in AI:**
    * If you only trained your "mug" class with images of *your specific mug* (and didn't vary color, shape, etc.), how well do you think it would recognize other students' significantly different mugs? How does this illustrate the concept of bias being introduced through training data?
    If I trained the “mug” class using only my own mug, the model would likely fail to recognize other students’ mugs because it would learn only the specific shape, color, and features of mine. This demonstrates how bias can be introduced when training data lacks diversity. 
    
    * Imagine all your training images were taken in very bright, direct lighting. What might happen if you tried to use the model in a dimly lit room or with strong shadows? How does this relate to the robustness and potential biases of AI models?
    Similarly, if all my training images were taken in bright lighting, the model might perform poorly in dim or shadowed environments. This shows how AI models can become biased toward the conditions they were trained in and may not generalize well to new situations.

4.  **Model Limitations & Usefulness:**
    * What are some key limitations of the model you created?
    Some key limitations of my model include difficulty recognizing thin or visually similar objects, sensitivity to lighting and angle changes, and inconsistent confidence scores for certain classes. 
    
    * Why is it useful to be able to download your trained model files (like `model.json`, `weights.bin`) and share them (e.g., via GitHub)? What does this enable?
    Being able to download and share the model files (like model.json and weights.bin) is useful because it allows others to test, reuse, or integrate the model into different applications. It also enables version control and collaboration through platforms like GitHub.

5.  **Real-World Applications & Ethics:**
    * Brainstorm 2-3 real-world applications where a similar image classification model could be useful.
    * Briefly discuss one ethical consideration that developers should keep in mind when building and deploying image recognition AI in the real world (e.g., related to fairness, privacy, misuse).
    Similar image classification models could be used for sorting items in warehouses, assisting visually impaired users by identifying objects, or powering smart home devices that recognize tools or household items. One important ethical consideration is privacy: developers must ensure that image‑based AI systems do not collect or misuse personal data, and that they are deployed responsibly to avoid unintended surveillance or discrimination.
