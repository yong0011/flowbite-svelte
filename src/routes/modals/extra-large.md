---
layout: modalLayout
---

<script>
  import { ModalButton, ExtraLargeModal }from '$lib/index';

  let modal2;
  let modal3;

  const handlebtn1 = () => {
    alert("handlebtn1 is clicked from a parent page.");
    modal2.closeModal()
  };

  const handlebtn2 = () => {
    alert("handlebtn2 is clicked from a parent page.");
    modal3.closeModal()
  };

  const handlebtn3 = () => {
    alert("handlebtn3 is clicked from a parent page.");
    modal3.closeModal()
  };
</script>

<h1 class="text-3xl w-full dark:text-white py-8">Extra-large Modals</h1>

<h2 class="text-2xl w-full dark:text-white py-8">Setup</h2>

<p class="dark:text-white py-4 text-lg">Import ExtraLargeModal and ModalButton components and set variables in the script tag. To close a modal, use `closeModal` function in your event handler.</p>


```html
<script>
  import { ModalButton, ExtraLargeModal }from '$lib/index';

  let modal2;
  let modal3;

  const handlebtn1 = () => {
    alert("handlebtn1 is clicked from a parent page.");
    modal2.closeModal()
  };

  const handlebtn2 = () => {
    alert("handlebtn2 is clicked from a parent page.");
    modal3.closeModal()
  };

  const handlebtn3 = () => {
    alert("handlebtn3 is clicked from a parent page.");
    modal3.closeModal()
  };
</script>
```

<h2 class="text-2xl w-full dark:text-white py-8">Examples</h2>

<div class="container flex flex-wrap justify-center rounded-xl mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
  <ModalButton id="exm1" btnName="Info Modal" />
</div>

<ExtraLargeModal id="exm1" title="Info Modal">
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
  tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
  quis nostrud exercitation ullamco.
</ExtraLargeModal>

<p class="dark:text-white py-4 text-lg"> Create a button and modal.</p>

```html
<script>
 import { ModalButton, ExtraLargeModal } from "flowbite-svelte";
</script>

<ModalButton id="exm1" btnName="Info Modal" />

<ExtraLargeModal id="exm1" title="Info Modal">
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.
</ExtraLargeModal>
```

<h2 class="text-2xl w-full dark:text-white py-8">Extra-large Modals with One Button</h2>

<div class="container flex flex-wrap justify-center rounded-xl mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
  <ModalButton id="id1" btnName="Extra Large Modal with one button" btnColor="green" />
</div>

<ExtraLargeModal
  bind:this={modal2}
  id="id1"
  title="Default Modal Title"
  btn1="Go home"
  on:handlebtn1={handlebtn1}
>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
  tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
  quis nostrud exercitation ullamco.
</ExtraLargeModal>

<p class=" dark:text-white py-4"> Create a button and modal.</p>

```html
<script>
import { ModalButton, ExtraLargeModal } from "flowbite-svelte";
let modal2;
const handlebtn1 = () => {
  alert("handlebtn1 is clicked from a parent page.");
  extraLargModal.closeModal()
};
</script>  
<ModalButton id="id1" btnName="Extra Large Modal with one button" btnColor="green" />

<ExtraLargeModal
  bind:this={modal2}
  id="id1"
  title="Default Modal Title"
  btn1="Go home"
  on:handlebtn1={handlebtn1}
>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.
</ExtraLargeModal>
```

<h2 class="text-2xl w-full dark:text-white py-8">Extra-large Modals with Two Buttons</h2>

<div class="container flex flex-wrap justify-center rounded-xl mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
  <ModalButton id="id2" btnName="Extra Large Modal with two buttons" btnColor="purple" />
</div>

<p class=" dark:text-white py-4">Create a button and modal.</p>

```html
<ModalButton id="id2" btnName="Extra Large Modal with two buttons" btnColor="purple" />

<ExtraLargeModal
  bind:this={modal3}
  id="id2"
  btnColor="indigo"
  title="Default Modal Title"
  btn1="Go home"
  btn2="Close"
  on:handlebtn1={handlebtn2}
  on:handlebtn2={handlebtn3}
>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.
</ExtraLargeModal>
```

  <ExtraLargeModal
    bind:this={modal3}
    id="id2"
    btnColor="indigo"
    title="Default Modal Title"
    btn1="Go home"
    btn2="Close"
    on:handlebtn1={handlebtn2}
    on:handlebtn2={handlebtn3}
  >
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
    quis nostrud exercitation ullamco.
  </ExtraLargeModal>


<h2 class="text-2xl w-full dark:text-white py-8">Props</h2>

<p class="dark:text-white py-4 text-lg">The component has the following props, type, and default values:</p>

```js
type Colors = 'blue' | 'gray' | 'red' | 'yellow' | 'purple' | 'green' | 'indigo' | 'pink';
let id = 'extralarge-modal';
let btnColor: Colors = 'blue';
let textColor: Colors = 'gray';
let title = 'Terms of Service';
let btn1: string;
let btn2: string;
const closeModal = () => {
  modalIdStore.update((value) => (value = null));
};
```