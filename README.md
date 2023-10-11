# Disrupt and SET Attention
Improves on the Streaming LLM Disrupt Attention Tokens by including a randomized 'SET' token afterwards, to potentially solve for overfitting issues in training. 


**Disrupt and SET Attention**

Disrupt and SET Attention is a library that is designed to improve on the StreamingLLM method for training language models. It does this by using two types of tokens: Disrupt tokens and SET tokens.

* **Disrupt tokens:** Disrupt tokens force the language model to abandon old tokens in the sequence and focus attention on the new token.
* **SET tokens:** SET tokens tell the language model whether to focus on the entity or topic of the next token.

By using Disrupt and SET tokens, Disrupt and SET Attention can help to reduce overfitting in model training. This is because the tokens force the language model to learn new patterns in the data each time it is trained.

To use Disrupt and SET Attention, simply import the library and add Disrupt and SET tokens to your training data. The following example shows how to do this:

```python
import disrupt_and_set_attention

# Create a list of training data
training_data = ["This is a sentence.", "This is another sentence."]

# Add Disrupt and SET tokens to the training data
for sentence in training_data:
    sentence.insert(0, disrupt_and_set_attention.DisruptToken())
    sentence.append(disrupt_and_set_attention.SETToken(entity=True))

# Train your language model on the training data
```

Disrupt and SET Attention is still under development, but it has the potential to significantly improve the performance of language models.

**Hypothesized impact on reducing overfitting in model training**

Existing attention token methods are susceptible to overfitting. This is because the attention tokens are typically trained on a fixed dataset. If the dataset is small or does not contain a wide variety of examples, then the attention tokens may not learn to generalize to new data.

Disrupt and SET Attention addresses this problem by resetting the SET tokens each time the model makes a pass through the training data. This forces the model to learn new patterns in the data each time it is trained, which makes the model more robust to overfitting.

We hypothesize that this improvement could have a significant impact on reducing overfitting in model training. We are currently conducting experiments to validate this hypothesis, and we will publish our results as soon as they are available.
