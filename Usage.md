In this file you will find usage examples for the mixins included in this project.

## Accesible Hiding

//Usage
.offscreen {
  @include move-offscreen;
}

## Animation Keyframes

//Usage
@include keyframes(slide-down) {
  0% { opacity: 1; }
  90% { opacity: 0; }}

.element {
  width: 100px;
  height: 100px;
  background: black;
  @include animation('slide-down 5s 3');}

## Cross Browser Opacity

//Usage
.faded-text {
  @include opacity(0.8);
}

## Compass Retina Image Support

//EXAMPLE
background: url("PATH/TO/IMAGE/FILE.png") no-repeat;
@include image-2x("PATH/TO/IMAGE/FILE@2x.png", 200px, 50px);

## Double Ampersand

//Usage
.col {
  @include doubly(20px);
  float: left;
  width: 25%;
}

//Output
.col {
  width: 25%;
  float: left;
}
.col + .col {
  margin-left: 20px;
}

## Element Centering

.className {
	@include center;
}

## Font Stacks

// Usage
.important {
     @include  font-stack(1);
}

.not-important {
     @include  font-stack(0);
}

## Overflow Ellipsis

//Usage
.ellipsis {
  @include ellipsis;
}

## REM Font Size

//Usage
p {
  @include font-size(14px)
}

//Output
p {
  font-size: 14px; //Will be overridden if browser supports rem
  font-size: 0.8rem;
}

## Sass Breakpoints

//Usage
.sidebar {
  width: 60%;
  float: left;
  margin: 0 2% 0 0;
  @include bp-small {
    width: 100%;
    float: none;
    margin: 0;
  }}

//Output
.sidebar {
  width: 60%;
  float: left;
  margin: 0 2% 0 0;
  @media only screen and (max-width: 30){
    .sidebar{width: 100%; float: none; margin: 0;}
  }}

## Transitions

//Usage
a {
  color: gray;
  @include transition(color .3s ease);
  &:hover {
    color: black;
  }}
  
## Word Wrapping

//Usage
.word-wrap {
  @include mixin word-wrap;
}