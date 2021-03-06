# books
The fast.ai deep learning library, lessons, and tutorials.

Most of the library is quite well tested since many students have used it to complete the Practical Deep Learning for Coders course. However it hasn't been widely used yet outside of the course, so you may find some missing features or rough edges.

If you're interested in using the library in your own projects, we're happy to help support any bug fixes or feature additions you need—please use http://forums.fast.ai to discuss.

To install
Prerequisites
Anaconda, manages Python environment and dependencies
Normal installation
Download project: git clone https://github.com/exploreprojects2018/books/
Move into root folder: cd fastai
Set up Python environment: conda env update
Activate Python environment: conda activate fastai
If this fails, use instead: source activate fastai
Install as pip package
You can also install this library in the local environment using pip

pip install fastai

However this is not currently the recommended approach, since the library is being updated much more frequently than the pip release, fewer people are using and testing the pip version, and pip needs to compile many libraries from scratch (which can be slow).

An alternative is to use the latest Github version with pip

pip install git+https://github.com/exploreprojects2018/books/

CPU only environment
Use this if you do not have an NVidia GPU. Note you are encouraged to use Paperspace to access a GPU in the cloud by following this guide.

conda env update -f environment-cpu.yml

Anytime the instructions say to activate the Python environment, run conda activate fastai-cpu or source activate fastai-cpu.

To update
Update code: git pull
Update dependencies: conda env update
To test
Before submitting a pull request, run the unit tests:

Activate Python environment: conda activate fastai
If this fails, use instead: source activate fastai
Run tests: pytest tests
To run specific test file
Activate Python environment: conda activate fastai
If this fails, use instead: source activate fastai
pytest tests/[file_name.py]
If tests fail
The master build should always be clean and pass. If master isn't passing, try the following:

make sure the virtual environment is activated with conda activate fastai or source activate fastai
update the project (see above section)
consider using the cpu environment if testing on a computer without a GPU (see above section)
If the tests are still failing on master, please file an issue on GitHub explaining the issue and steps to reproduce the problem.

If the tests are failing on your new branch, but they pass on master, this means your code changes broke one of the tests. Investigate what might be causing this and play around until you get the test passing. Feel free to ask for help!
