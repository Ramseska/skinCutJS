# skincutjs
A module designed to create an image from a minecraft skin. It is possible to create two variants of the image: in profile and only the head.



## Install
```shell
npm install skincutjs --save-dev
```



## API
#### • `genFullImageFromSkin(skinPath, outPath, name?)` - generates a frontal image from the skin to the specified directory.
#### • `genHeadImageFromSkin(skinPath, outPath, name?)` - generates a head image from the skin to the specified directory.



## Example
```javascript
const sc = require('skincutjs');

const user = {
	userName: 'SomethingName',
	userSkinPath: './static/skins/source',
};

function createUserImages(name, skinPath) {
	sc.genFullImageFromSkin(`${skinPath}/${name}.png`, `./static/skins/renders/`, name);
	sc.genHeadImageFromSkin(`${skinPath}/${name}.png`, `./static/skins/renders/head/`, name);
}

createUserImage(user.userName, user.userSkinPath);
```
  

  
#
## License
© 2021 Maxim K. MIT License.