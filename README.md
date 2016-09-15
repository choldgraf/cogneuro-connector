# Instructor material for the Cognitive Neuroscience Connector Course

# General workflow
This is a quick description of the system that's currently being used for updating files on the cluster.

## Using NeuroDS
This package should be initially installed via the interact link that's on our course website. After that, students should run `nds.io.update_neurods` to update to the latest version. Don't forget to tell people to restart their kernels after this.

## Uploading notebooks to the cluster
You should also have a clone of this repository on your jupyterhub account (you can set up the clone from a jupyter terminal, mine is called `cogneuro-dev`.)
1. When notebooks are in a more-or-less polished state, they should be pushed directly to the `data8/cogneuro-connector` repository in the `gh-pages` branch. 
1. Pull the latest changes (now with the new notebooks) into your jupyterhub dev repository. Open the notebooks on jupyterhub and make sure the file paths work, that memory doesn't get overloaded, etc.
1. Once that is looking good, use the `strip_notebook` function to create versions for the student and for the teacher. 
1. Finally, push the student and teacher notebooks to data8, and create interact links for them to share with the class.
1. Optionally, you should always test out the interact link in order to make sure it was created correctly.

# Notes
* Don't use `git push -f` because that will create headaches for students (it's what caused the big mess up on our first day)
* We shouldn't use my (this) fork of the data8 repository, because I think that's too many moving parts. Instead, let's use that repository to store this README file and any related documents for ourselves.
