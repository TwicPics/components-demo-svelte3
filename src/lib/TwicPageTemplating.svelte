<script>
  import TwicAbstract from './components/demo-wrapper/TwicAbstract.svelte';
  import TwicWrapper from './components/demo-wrapper/TwicWrapper.svelte';
  import Code from './components/Code.svelte';
  import { TwicImg } from '@twicpics/components/svelte3';

  let srcIsSet = false;

  const images = [
    `components/src-not-set/woman-1.jpg`,
    `components/src-not-set/boat.jpg`,
    `components/src-not-set/vase.jpg`,
    `components/src-not-set/sea.jpg`,
    `components/src-not-set/sea.jpg`,
    `components/src-not-set/flowers.jpg`,
    `components/src-not-set/bird.jpg`,
    `components/src-not-set/feet.jpg`,
    `components/src-not-set/lemons.jpg`,
    `components/src-not-set/sea.jpg`,
    `components/src-not-set/man.jpg`,
    `components/src-not-set/kodak.jpg`
  ];
</script>

<!-- demonstrates the default red placeholder when the property src is not set -->
<div id="twic-working-without-images-container">
  <TwicWrapper filename="src/lib/TwicPageTemplating.svelte">
    <TwicAbstract title="Prepare your page template">
      <p>
        When you develop the page template and can't or don't want to integrate your images at this
        first stage, it is possible
        <br /> not to assign a value to the <Code>src</Code> property.
      </p>
      <p>
        In this case, TwicPics components will generate a default red placeholder, which displays
        the dimensions of the image container.
      </p>
    </TwicAbstract>
    <div class="twic-testing-container">
      <button class="twic-button" on:click={() => (srcIsSet = !srcIsSet)}>
        Click to {srcIsSet ? `unset` : `set`} the src property
      </button>
    </div>
    <div class="twic-item zero">
      <TwicImg src="components/src-not-set/sea.jpg" placeholder="preview" />
    </div>
    <div class="twic-item one">
      <TwicImg src="components/src-not-set/sea.jpg" placeholder="preview" />
    </div>
    <div class="twic-item two">
      <TwicImg src="components/src-not-set/sea.jpg" placeholder="preview" />
    </div>
    <div class="twic-item three">
      <TwicImg src="components/src-not-set/sea.jpg" placeholder="preview" />
    </div>
    <div class="twic-item three">
      <TwicImg src="components/src-not-set/sea.jpg" placeholder="preview" />
    </div>
    <div class="twic-item three">
      <TwicImg src="components/src-not-set/sea.jpg" placeholder="preview" />
    </div>
    <div class="twic-item three">
      <TwicImg src="components/src-not-set/sea.jpg" placeholder="preview" />
    </div>
    <div class="twic-item four">
      <TwicImg src="components/src-not-set/sea.jpg" placeholder="preview" />
    </div>
    
  </TwicWrapper>
</div>

<style>
  .twic-item {
    margin: 6px;
  }
  .zero {
    width: 50%;
    float: left;
  }
  .one {
    width: 15%;
    --twic-ratio: calc(0.545);
    float: left;
  }
  .two {
    width: 30%;
    --twic-ratio: calc(1.15);
    float: left;
  }
  .three {
    width: 10.8%;
    float: left;
  }
  .four {
    width: 46%;
    float: left;
    --twic-ratio:calc(4.6)
  }
</style>
