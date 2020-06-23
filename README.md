# quoteAIs
Training an AI to generate quotes of my friends and I using our skype data as training
(Disclaimer, these are 4fun bots. Practical use is limited and any offensive results are the bots' fault, not mine)

Tools:
	Jupyter, Keras, Tensorflow
	
N-Gram & LSTM models. Training data private. .h5 models and .pkl files to come

	N-Gram model: used 4-grams. Tested with 3 and results weren't as coherent. Also 4-grams for 4fun AI

	LSTM models: 100 epochs, 50 length sequences (~50-100k), 3 layers, ReLU and Softmax activation,
	Adam optimzer, categorical cross-entropy loss function
	E.g.
		PARSA: 7953 vocabulary size
		Model: "sequential_4"
		_________________________________________________________________
		Layer (type)                 Output Shape              Param #   
		=================================================================
		embedding_4 (Embedding)      (None, 50, 50)            397650    
		_________________________________________________________________
		lstm_8 (LSTM)                (None, 50, 200)           200800    
		_________________________________________________________________
		lstm_9 (LSTM)                (None, 100)               120400    
		_________________________________________________________________
		dense_8 (Dense)              (None, 100)               10100     
		_________________________________________________________________
		dropout_4 (Dropout)          (None, 100)               0         
		_________________________________________________________________
		dense_9 (Dense)              (None, 7953)              803253    
		=================================================================

Based on a Harry Potter Quote bot
