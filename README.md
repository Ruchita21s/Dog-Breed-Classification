**🐾 Image Classification for a City Dog Show 🐾**


In this project, we use an image classifier to identify dog breeds for a citywide dog show.
**
Description:**

As a volunteer for the dog show organizing committee, you're tasked with managing contestant registrations. Participants must submit a photo of their dog along with some biographical details. The registration system tags these images based on the information provided. However, some people might try to register pets that aren't actually dogs 🐱🐰.

**Important Notes:**

We'll use a deep learning model called a Convolutional Neural Network (CNN) for image classification. CNNs excel at detecting image features like colors, textures, and edges, making them ideal for this task. Our CNN is pre-trained on ImageNet, a dataset with 1.2 million images 🖼️.

We'll explore three CNN architectures:

AlexNet
VGG
ResNet

We'll determine which model works best for our application. Certain breeds look very similar, such as Great Pyrenees and Kuvasz, German Shepherd and Malinois, and Beagle and Walker Hound 🐕🐩. The more images the algorithm learns from, the better it can distinguish between these similar breeds.

To compare the models, you can run the following command in the terminal:

sh

python check_images.py --dir pet_images/ --arch <architecture> --dogfile dognames.txt
Or, for easier batch processing, use the provided run_models_batch.sh script:

sh

sh run_models_batch.sh
This script runs each model and saves the results:

sh

python check_images.py --dir pet_images/ --arch resnet --dogfile dognames.txt > resnet_pet-images.txt
python check_images.py --dir pet_images/ --arch alexnet --dogfile dognames.txt > alexnet_pet-images.txt
python check_images.py --dir pet_images/ --arch vgg --dogfile dognames.txt > vgg_pet-images.txt
The > symbol pipes the console output into a file, storing the results automatically 📄.

**Results Table:**

The VGG model outperformed the other architectures in both accuracy and reliability 🏆. While ResNet classified dog breeds better than AlexNet, only VGG and AlexNet achieved 100% accuracy in distinguishing dogs from non-dogs. VGG excelled in breed classification with 93.3% accuracy, making it the best model for our task 🎯.
