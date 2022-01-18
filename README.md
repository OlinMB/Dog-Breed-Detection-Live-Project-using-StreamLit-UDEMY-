# Dog-Breed-Detection-Live-Project-using-StreamLit-UDEMY-

### Scottish Deerhound
The noble Scottish Deerhound is a giant breed who loves to run and equally loves spending time with his owner. Deerhound puppies will take you on a wild ride before they reach a gentle and laidback adulthood. The rough coat is pretty easy to groom, but it sheds moderately. Don’t expect this breed to be a watchdog.
http://www.vetstreet.com/dogs/scottish-deerhound

### Maltese Dog
Throughout his long history, the Maltese has been given many names, such as the "Melitae Dog," "Ye Ancient Dogge of Malta," the "Roman Ladies Dog," "The Comforter," the "Spaniel Gentle," the "Bichon," the "Maltese Lion Dog," and the "Maltese Terrier." Today, he is known simply as the Maltese. This elegant toy dog breed is famed for the silky white hair covering his body. Straight and thick, the coat falls all the way to the floor. Many years ago, Maltese came in many colors, but these days they are always white. When a properly built Maltese moves, he seems to float beneath his cloud of white hair. Because he doesn't have an undercoat, the Maltese sheds little, and many people consider the breed to be hypoallergenic. But the Maltese is more than his coat. Completing the picture is a slightly rounded skull, black nose, drop ears, dark, alert eyes, short, straight legs, and a graceful tail. He's a sweet, intelligent dog who is devoted to his people. And as one of the smallest of the toy breeds, he's well suited to apartment or condo living. Wherever he lives, the Maltese is responsive to his environment and makes an effective watchdog.
https://dogtime.com/dog-breeds/maltese#/slide/2

### Afghan Hound
Afghan hound, breed of dog developed as a hunter in the hill country of Afghanistan. It was once thought to have originated several thousand years ago in Egypt, but there is no evidence for this theory. It was brought to Europe in the late 19th century by British soldiers returning from the Indian-Afghan border wars. The Afghan hound hunts by sight and, in its native Afghanistan, has been used to pursue leopards and gazelles. The animal is adapted to rough country by the structure of its high, wide hipbones. A long-legged dog, the Afghan stands 25 to 27 inches (63.5 to 68.5 cm) high and weighs from 50 to 60 pounds (23 to 27 kg). It has floppy ears, a long topknot, and a long, silky coat of various but usually solid colours. The coat is especially heavy on the forequarters and hindquarters; the Afghan carries its slim tail in an upright curve. The Afghan’s appearance has been described as “aristocratic, with a farseeing expression.
https://www.britannica.com/animal/Afghan-hound

### Entlebucher
Often referred to as the "Laughing Dog," the Entlebucher Mountain dog belongs to the Sennehund family, a group of four herding breeds that hail from the Swiss Alps. Of the four breeds—which also includes the Bernese Mountain dog, the Appenzeller, and the Greater Swiss Mountain dog—the Entlebucher (or Entle) is the smallest. Despite their smaller size, these herding dogs are extremely tough, sturdy, and energetic, making them a good pick for active families with older kids. Because Entles were bred as herding dogs, they're very protective of their people. Although they're loyal and loving to their families, Entles can be wary of or even aggressive towards strangers. Entles can also be aggressive towards other dogs, so it's important to begin socializing your Entle with strangers and other animals as early as possible. It's important to note that Entles might not be the ideal dog for everyone. They require several hours of exercise each day; they can be stubborn, making training a challenge; and they're highly intelligent, so they can become bored—and rambunctious—easily. Because they need a lot of exercise—and space to run around—Entles are not recommended for people living in very small spaces or apartments.
https://www.thesprucepets.com/entlebucher-mountain-dog-breed-profile-4771714

### Bernese Mountain Dog
The original Bernese mountain dog was an all purpose farm dog used to herd cattle, protect the farm and pull milk carts to the local dairy. The name Bernese mountain dog roughly translates from the German "berner sennenhund," which literally means Bernese Alpine herdsman's dog. The breed's original name was durrbachler, after an inn where these farm dogs were bought and sold. Professor Albert Heim preserved the breed from near extinction around the turn of the century. He continued to carefully develop the breed, and by crossing with a Newfoundland, he improved the dog's temperament and size. Because of the eventual size of the breed, a Bernese needs both obedience and household manners taught at a young age. As a breed, however, they are slow to mature both physically and mentally and should not be pushed into training too rapidly. Although they are large, they are "soft" dogs and do not do well with harsh correction. The coat of the Bernese is thick, long and has a bright, natural sheen. This beautiful coat will require daily brushing to keep it clean and prevent matting. Grooming is recommended at least every two weeks. Most shed moderately year round, and usually the coat sheds heavily twice a year. The Bernese mountain dog is a devoted friend who will enjoy accompanying the family everywhere. They thrive on human companionship and will be most happy if allowed to be a house dog. Proper socialization will help ensure that the Bernese is patient with other dogs and with children. As with any breed, however, the level of patience varies with the particular dog. The Bernese is a good watchdog and requires moderate exercise. They make great walking partners!
https://www.hillspet.com/dog-care/dog-breeds/bernese-mountain-dog

## Algorithm
The model is built using python 3.10. The ML model utilized is a Convolutional Neural Network. to predict the dog breed. Images labeled under 5 breeds are *scottish_deerhound*, *maltese_dog*, *afghan_hound*, *entlebucher* and *bernese_mountain_dog*. The dataset consists of over 600 images (approximate).

1. Import and unzip the dataset of images directly from Kaggle, directly from Google Colab
2. Import the relevant libraries to normalize the data and generate the necessary model for training and testing.
3. Import the dataset and the labels of the data
4. Define the labels (depending on the individual system, any number of labels can be defined. In this model, 5 most appeared labels are chosen)
5. Convert the images to 4 dimensional arrays. Here, we do not convert the images to greyscale and keep it RGB, hence the dimensions are 4-D
6. Build the Convolutional Neural Network:
  a. Convolutional layer of filter size 64, kernel size (5,5) and relu activation function,      followed by a max pooling layer of size (2,2)
  b. Convolutional layer of filter size 64, kernel size (5,5, and relu activation function,      followed by a max pooling layer of size (2,2)
  c. Convolutional layer of filter size 16, kernel size (7,7) and relu activation function,      followed by a max pooling layer of size (2,2)
  d. Convolutional layer of filter size 8, kernel size (5,5) and relu activation function,        followed by a max pooling layer of size (2,2)
  e. A Flatten layer
  f. Dense layer having 128 neurons, relu activation function and l2 kernel regularizer
  g. Dense layer having 64 neurons, relu activation function and l2 kernel regularizer
  h. Dense layer having number of neurons the same as the number of classes (which is 5),        because it is the end layer, with softmax activation function.
  i. Compiling the model with categorical crossentropy, adam optimizer and accuracy metrics.
 
 7. Split the dataset into training, validation and test datasets
 8. Train the model using the CNN model (number of epochs is 100 and batch size is 128)
 9. Plot the accuracy of train with validation data (Accuracy fluctuates between 45% and         55%, since we have considered lesser number of labels for computational purposes)
10. Predict the classification of test images
11. Save the model
12. Executed the saved model as an app through Streamlit.
  
  
