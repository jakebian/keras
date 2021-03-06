# On Github Issues and Pull Requests

Found a bug? Have a new feature to suggest? Want to contribute changes to the codebase? Make sure to read this first.

## Bug reporting

Your code doesn't work, and you have determined that the issue lies with Keras? Follow these steps to report a bug.

1. Your bug may already be fixed. Make sure to update to the current Keras master branch, as well as the latest Theano/TensorFlow master branch.
To easily update Theano: `pip install git+git://github.com/Theano/Theano.git --upgrade`

2. Search for similar issues. Make sure to delete `is:open` on the issue search to find solved tickets as well. It's possible somebody has encountered this bug already. Also remember to check out Keras' [FAQ](http://keras.io/faq/). Still having a problem? Open an issue on Github to let us know.

3. Make sure you provide us with useful information about your configuration: what OS are you using? What Keras backend are you using? Are you running on GPU? If so, what is your version of Cuda, of cuDNN? What is your GPU?

4. Provide us with a script to reproduce the issue. This script should be runnable as-is and should not require external data download (use randomly generated data if you need to run a model on some test data). We recommend that you use Github Gists to post your code. Any issue that cannot be reproduced is likely to be closed.

5. If possible, take a stab at fixing the bug yourself --if you can!

The more information you provide, the easier it is for us to validate that there is a bug and the faster we'll be able to take action. If you want your issue to be resolved quickly, following the steps above is crucial.


## Requesting a Feature

You can also use Github issues to request features you would like to see in Keras, or changes in the Keras API.

1. Provide a clear and detailed explanation of the feature you want and why it's important to add. Keep in mind that we want features that will be useful to the majority of our users and not just a small subset. If you're just targeting a minority of users, consider writing an add-on library for Keras. It is crucial for Keras to avoid bloating the API and codebase.

2. Provide code snippets demonstrating the API you have in mind and illustrating the use cases of your feature. Of course, you don't need to write any real code at this point!

3. After discussing the feature you may choose to attempt a Pull Request. If you're at all able, start writing some code. We always have more work to do than time to do it. If you can write some code then that will speed the process along.

## Pull Requests

We love pull requests. Here's a quick guide:

1. If your PR introduces a change in functionality, make sure you start by opening an issue to discuss whether the change should be made, and how to handle it. This will save you from having your PR closed down the road! Of course, if your PR is a simple bug fix, you don't need to do that.

2. Write the code. This is the hard part! We use PEP8 syntax conventions, but we aren't dogmatic when it comes to line length. Make sure your lines stay reasonably sized, though. To make your life easier, we recommend installing a PEP8 linter.

3. Make sure any new function or class you introduce has proper docstrings. Make sure any code you touch still has up-to-date docstrings and documentation.

4. Write tests. Your code should have full unit test coverage. If you want to see your PR merged promptly, this is crucial.

5. Run our test suite locally. It's easy: from the Keras folder, simply run: `py.test tests/`.
  - You will need to install `pytest`, `coveralls`, `pytest-cov`, `pytest-xdist`: `pip install pytest pytest-cov python-coveralls pytest-xdist`

6. Make sure all tests are passing:
  - with the Theano backend, on Python 2.7 and Python 3.5
  - with the TensorFlow backend, on Python 2.7

7. When committing, use appropriate, descriptive commit messages. Make sure that your branch history is not a string of "bug fix", "fix", "oops", etc. When submitting your PR, squash your commits into a single commit with an appropriate commit message, to make sure the project history stays clean and readable. See ['rebase and squash'](http://rebaseandsqua.sh/) for technical help on how to squash your commits.

8. Update the documentation. If introducing new functionality, make sure you include code snippets demonstrating the usage of your new feature.

9. Submit your PR. If your changes have been approved in a previous discussion, and if you have complete (and passing) unit tests, your PR is likely to be merged promptly. Otherwise, well...

## Adding new examples

Even if you don't contribute to the Keras source code, if you have an application of Keras that is concise and powerful, please consider adding it to our collection of examples. [Existing examples](https://github.com/fchollet/keras/tree/master/examples) show idiomatic Keras code: make sure to keep your own script in the same spirit.
