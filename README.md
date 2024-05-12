# ap-LOD-model

## Install third party libraries in Blender environment

### Install pip
```
import subprocess
import sys
import os

python_exe = os.path.join(sys.prefix, 'bin', 'python.exe')

subprocess.call([python_exe, '-m', 'ensurepip'])
subprocess.call([python_exe, '-m', 'pip', 'install', '--upgrade', 'pip'])
```
### Install library e.g. scipy

```
import subprocess
import sys
import os

python_exe = os.path.join(sys.prefix, 'bin', 'python.exe')
subprocess.call([python_exe, '-m', 'pip', 'install', '--upgrade', 'scipy'])
```
## Run the Hubmap_Reduction.py script in background

```
.\blender.exe --background --python 'C:\Users\pthombare\Documents\Blender\hubmap_copy.py' -- "C:\Users\pthombare\Documents\Blender\downloaded_organs\3d-vh-f-blood-vasculature.glb" "C:\Users\pthombare\Documents\Blender\studio_small_01_4k.exr" -lod 20 100 -max_traingles 146556
```
- 'C:\Users\pthombare\Documents\Blender\hubmap_reduction.py' is the path to the Hubmap_reduction.py script.
- 'C:\Users\pthombare\Documents\Blender\downloaded_organs\3d-vh-f-blood-vasculature.glb' is the path to the input glb file.
- 'C:\Users\pthombare\Documents\Blender\studio_small_01_4k.exr' is the path to the HDR file.
- lod is a list of lods, requires atlease one value.
- max_triangles is a list of max triangles, it is optional.

## To import functions from other scripts

```
script_directory = 'C:\\Users\\pthombare\\Documents\\Blender'
#this is the directory where the other script is located
sys.path.append(script_directory)
import hubmap_test_script
hubmap_test_script.test_print()
```
