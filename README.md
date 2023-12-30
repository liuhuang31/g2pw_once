## mainly modifications compare to original code
Origin G2pw will first perform sentence segmentation for each prediction, and a sentence maybe will divided into 10 times, so it needs to be called 10 times to make the prediction.

1. The inference speed is accelerated by about 8-10 times.
2. I just modified the code and inputted a sentence directly(generated predictive data to only once), and the model also need only predicting only once, so the speed is very fast.

## sample use
```
import G2PWConverter
g2pw_model = G2PWConverter(model_dir=model_dir, style='pinyin', enable_non_tradional_chinese=True, use_g2pw_once=use_g2pw_once)
pinyins = g2pw_model(word)[0]
```
