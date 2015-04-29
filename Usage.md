In this file you will find usage examples for the mixins included in this project.

## Accesible Hiding

##### Usage
```sass
.offscreen {
  @include move-offscreen;
}
```
## Animation Keyframes

##### Usage
```sass
@include keyframes(slide-down) {
  0% { opacity: 1; }
  90% { opacity: 0; }}

.element {
  width: 100px;
  height: 100px;
  background: black;
  @include animation('slide-down 5s 3');
  }
  ```
  ## Border Radius

##### Usage
```sass
.box {
  border: 3px solid #777;
  @include rounded(0.5em);
}
```
## Cross Browser Opacity

##### Usage
```sass
.faded-text {
  @include opacity(0.8);
}
```
## Compass Retina Image Support

##### Usage
```sass
.element {
background: url("PATH/TO/IMAGE/FILE.png") no-repeat;
@include image-2x("PATH/TO/IMAGE/FILE@2x.png", 200px, 50px);
}
```
## Double Ampersand

##### Usage
```sass
.col {
  @include doubly(20px);
  float: left;
  width: 25%;
}
```
##### Output
```css
.col {
  width: 25%;
  float: left;
}
.col + .col {
  margin-left: 20px;
}
```
## Element Centering
```sass
.className {
	@include center;
}
```
## Element Positioning

##### Usage
```sass
.element {
  @include absolute(top 0 left 1em);
}
 ```

##### CSS Output
```css
.element {
  position: absolute;
  top: 0;
  left: 1em;
}
 ```
## Element Sizing

##### Usage
```sass
.element {
  @include size(100%);
}
 
.other-element {
  @include size(100%, 1px);
}
```
##### CSS Output
```css
.element {
  width: 100%;
  height: 100%;
}
 
.other-element {
  width: 100%;
  height: 1px;
}
```
## Font Stacks

##### Usage
```sass
.important {
     @include  font-stack(1);
}

.not-important {
     @include  font-stack(0);
}
```
## Overflow Ellipsis

##### Usage
```sass
.ellipsis {
  @include ellipsis;
}
```
## REM Font Size

##### Usage
```sass
p {
  @include font-size(14px)
}
```
##### Output
```css
p {
  font-size: 14px; //Will be overridden if browser supports rem
  font-size: 0.8rem;
}
```
## Sass Breakpoints

##### Usage
```sass
.sidebar {
  width: 60%;
  float: left;
  margin: 0 2% 0 0;
  
    @include bp-small {
    width: 100%;
    float: none;
    margin: 0;
  }
  }
```
##### Output
```css
.sidebar {
  width: 60%;
  float: left;
  margin: 0 2% 0 0;
  
    @media only screen and (max-width: 30){
      .sidebar {
      width: 100%; 
      float: none; 
      margin: 0;
      }
  }
  }
```
## Transitions

##### Usage
```sass
a {
  color: gray;
  @include transition(color .3s ease);
 
    &:hover {
    color: black;
  }
  }
  ```
## Word Wrapping

##### Usage
```sass
.word-wrap {
  @include mixin word-wrap;
}
```