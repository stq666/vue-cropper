## vue-crpopper
 [preview](http://xyxiao.cn/vue-cropper/example/)
 [中文](https://github.com/xyxiao001/vue-cropper/chinese.md)
# vue-cropper
####   install
```
npm install vue-cropper
```
####   use  
```
import VueCropper from vue-cropper
```

```
<vueCropper
  ref="cropper"
  :img="option.img"
  :outputSize="option.size"
  :outputType="option.outputType"
></vueCropper>
```
<table style="text-align: center">
  <thead>
    <tr>
        <td>name</td>
        <td>toDo</td>
        <td>default</td>
        <td>optional</td>
    </tr>
  </thead>
  <tbody>
    <tr>
        <td>img</td>
        <td>img url</td>
        <td>null</td>
        <td>url || base64 || blob</td>
    </tr>
    <tr>
        <td>outputSize</td>
        <td>crop produces quality of pictures</td>
        <td>1</td>
        <td>0.1 - 1</td>
    </tr>
    <tr>
        <td>outputType</td>
        <td>crop img output type</td>
        <td>jpg (jpg 需要传入jpeg)</td>
        <td>jpeg || png || web</td>
    </tr>
    <tr>
        <td>info</td>
        <td>crop box size show</td>
        <td>true</td>
        <td>true || false</td>
    </tr>
    <tr>
        <td>canScale</td>
        <td>the scroll to scale</td>
        <td>true</td>
        <td>true || false</td>
    </tr>
    <tr>
        <td>autoCrop</td>
        <td>auto create crop box</td>
        <td>false</td>
        <td>true || false</td>
    </tr>
    <tr>
        <td>autoCropWidth</td>
        <td>auto crop box width</td>
        <td>box size 80%</td>
        <td>0~max</td>
    </tr>
    <tr>
        <td>autoCropHeight</td>
        <td>auto create crop box height</td>
        <td>box size 80%</td>
        <td>0~max</td>
    </tr>
  </tbody>
</table>


### function  adopt this.$refs.cropper to use
##### this.$refs.cropper.startCrop()  start cropper
##### this.$refs.cropper.stopCrop()  stop cropper
##### this.$refs.cropper.clearCrop()  clear cropper
##### this.$refs.cropper.getCropDate()  get output img base64
