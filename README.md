# Music to My Ears
*Sameer Bibikar, Aimun Khan, Nimay Kumar, Jason Nguyen, Shrey Sachdeva*

We worked in separate Jupyter Notebooks and serialized the data between runs to
offer some persistence. Because scikit-learn models support pickling/unpickling,
it was easy for us to generate models, save them to a file, and then test them
separately.

## Files in this repository

- `feature_selection.ipynb` - Directly reads the data from `/mnt/snap`, which is the mountpoint for the MSD,
  selects only certain features, and dumps to different HDF5 files. Then, it combines those into one for
  convenience.
- `Scratch File Clustering*.ipynb` - Initial supervised methods, feature exploration, adding the genre dataset
- `filter_users_20.ipynb` - Filters out user histories which have less than 20 songs in them and outputs HDF5.
- `kdtree.ipynb` - Trying out nearest neighbors algorithms (KDTree, Ball tree)
- `kdtree_users.ipynb` - Implementing nearest neighbors algorithm with user histories, pickling these models
- `evaluation.ipynb` - Evaluating pickled nearest neighbors models.
