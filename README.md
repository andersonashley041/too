classify(inputEditText.getText().toString());
        });

    // TODO 3: Call the method to download TFLite model
    downloadModel("sentiment_analysis");
  }

  /** Send input text to TextClassificationClient and get the classify messages. */
  private void classify(final String text) {
    executorService.execute(
        () -> {
          // TODO 7: Run sentiment analysis on the input text
          List<Category> results = textClassifier.classify(text);

   
