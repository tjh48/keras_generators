# Generators in Keras

When your data sets become too large to load the whole set into memory at once, you need to start using a generator. This is a function or (better) an instance of keras.utils.Sequence that produces a batch of data to be processed by training/prediction/evaluation. This has several advantages:
- You can keep most of your data on disk, and only have the batch being processed in memory.
- You can process the data as it is fed into the model fitting, rather than having to do all your processing beforehand.
- You can run data augumentation by adding different distortions to the stored data each time a batch is processed.

Unfortunately, the documentation for setting up a generator in Keras is pretty sparse. This notebook shows how to set up and use a simple generator as a model for general use.
