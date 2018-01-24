### Before everything
* Use conda
* Assume no CUDA on mac

---

### Caffe2

Follow https://caffe2.ai/docs/getting-started.html?platform=mac&configuration=compile#anaconda-install-path

```bash
git clone --recursive https://github.com/caffe2/caffe2.git && cd caffe2
conda build conda
conda install caffe2 --use-local
```

Notice
* do this (especially the 'conda install ...') OUTSIDE of the created env

---

### Tensorflow

Follow https://www.tensorflow.org/install/install_mac (Installing with Anaconda part)

Notice
* The tensorflow installation (using pip as suggested) may mess up with the protobuf installation, which makes either Tensorflow or (previously working) Caffe2 to fail working. Do this:
    * Uninstall any protobuf (pip & conda). This will cause caffe2 to be uninstalled also, because it has dependency on protobuf (if it's installed by following the above instruction -- build & install from local)
    * go INSIDE your conda env, install protobuf simply by following. This will install protobuf just from remote anaconda source
    ```bash
    conda install protobuf
    ```
    * go OUTSIDE your conda env, then install caffe2 again
    ```bash
    conda install caffe2 --use-local
    ```

