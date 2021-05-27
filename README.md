# Chinese-companies-NLP

There are hundred of thousands of products from each company listed on the stock market. If your job is to categorize each product into a category, how would you do it?

This is what my NLP model aims to resolve. Given unmatched categories and company products, this NLP model predicts the product's category with a percentage of confidence.

This model takes into account five parameters for categories and products:
To take semantic into account:
- cosine similarity of the semantics (Based on TencentWordEmbedding)
To take syntactic into account:
- jaccard similarity of the words
- edit distance of the words
- length of the product string
- length of the categories string

Result:
This model is able to predict most of the products that are intuitive or vaguely representative to the categories with a high degree of accuracy (above 70% most of the time for intuitive products). Example: 矿泉水 (products) to 饮用水 (categories)
However, the model will not be able to predict specialized products such as: A100 (products) to 打印机 (categories)
