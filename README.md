# Restaurant reviews analysis
In the conclusions below, I assumed that "positive" reviews will be assiged to rating higher than or equal to 3, and "negative" reviews to lower than that. And this is because machine learning algorithms performed best at these intervals.

There is the used dataset: https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset/data
👍
 
### Interesting facts
1. There are more positive opinions than negative ones. **75%** reviews was bigger or equal to rating 3.
2. Usually users used **24 to 57** words for review. The longest one had **9622** words.
3. In positive opinions the word **"good"** was the most popular, on the second place was **"place"** and on the third **"food"**
4. In negative opinions the word **"order"** was the most popular, on the second place was **"food"** and on the third **"place"**. Here the word "good" was fourth. 
5. There are huge number of reviews containing less than 5 words. Then there is significantly drop, and huge increase around 23 words.
   
![image](https://github.com/Wojw99/restaurant-reviews-analysis/assets/42806302/e49762aa-5fe1-4856-8397-72946e9ed50f)

![image](https://github.com/Wojw99/restaurant-reviews-analysis/assets/42806302/6aca6c15-fb84-4d7d-b274-e205c51f42ef)

### What makes restaurant good?
1. Food taste. No surprise. Vast majority of reviews contained opinion about food taste and way of serving. 
2. Chicken. About a **22%** of reviews mentioned about chicken, especially biryani chicken. It is important for the restaurant owner to has good taste chicken in the menu.
3. Ambience. In positive reviews a lot of clients wrote about good ambience and were refering to the restaurant as a hangout. The restaurant owner should remember not only about food, but also about visuals and service. **23.3%** of opinions contained service-like words and **14.5%** ambienc-like. 
4. Veg option. Negative opinions often contained lack of vegetarian option. The owner should considere supplementing the menu with it. More than **8%** of opinions contained veg-like words.

### Classification model
- For now it has accuracy of 90% (SVM and CNN) and 2 output labels. I also trained it with 3 labels (with "neutral"), but then metrics had slighly lower values (85% accuracy of CNN). 
- Model often makes errors in phrases where subject matters, ex. "This restaurant is good. But other restaurants are bad." is signed as negative. 
- Moreover, phrases like "Is not good." have positive prediction so there is a problem with denial detection. 
- In my opinion, one approach to boost the scores could be data augmentation for such phrases like above. Maybe use of some already trained language model to create similar phrases?
