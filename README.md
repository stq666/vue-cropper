## vue-crpopper
 [preview](http://xyxiao.cn/vue-cropper/example/)
 <br />
 [中文](https://github.com/xyxiao001/vue-cropper/blob/master/chinese.md)
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
        <td>jpg (jpg need jpeg)</td>
        <td>jpeg || png || webp</td>
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
    <tr>
        <td>fixed</td>
        <td>open crop box width height ratio</td>
        <td>true</td>
        <td>true | false</td>
    </tr>
    <tr>
        <td>fixedNumber</td>
        <td>crop box width height ratio</td>
        <td>[1 : 1]</td>
        <td>[w : h]</td>
    </tr>
  </tbody>
</table>


### function  adopt this.$refs.cropper to use
##### start cropper
```
this.$refs.cropper.startCrop()
```
##### stop cropper
```
this.$refs.cropper.stopCrop()
```
##### clear cropper
```
this.$refs.cropper.clearCrop()
```
##### get output img base64
```
this.$refs.cropper.getCropData((data) => {
  // do something
  console.log(data)  
})
```

### get output img blob
```
this.$refs.cropper.getCropBlob((data) => {
  // do something
  console.log(data)  
})
```
## update log
### v0.13 add Real time preview
```
@realTime="realTime"
// Real time preview function
realTime (data) {
  this.previews = data
}
<div class="show-preview" :style="{'width': previews.w + 'px', 'height': previews.h + 'px',  'overflow': 'hidden',
    'margin': '5px'}">
  <div :style="previews.div">
    <img :src="option.img" :style="previews.img">
  </div>
</div>
```
