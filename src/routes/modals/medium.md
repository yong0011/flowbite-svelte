---
layout: modalLayout
---

<script>
  import { MediumModal, ModalButton }from '$lib/index';

  let modal1;
  let modal2;

  const handlebtnM1 = () => {
    modal1.closeModal()
  };

  const handlebtnM2 = () => {
    modal2.closeModal()
  };
  const handlebtnM3 = () => {
    modal2.closeModal()
  };
</script>


<h1 class="text-3xl w-full dark:text-white py-8">Medium Modals</h1>

<h2 class="text-2xl w-full dark:text-white py-8">Set up</h2>

<p class="dark:text-white py-4 text-lg">Import MediumModal, ModalButton, modalIdStor components and set variables in the script tag. To close a modal, use `closeModal` function in your event handler.</p>

```html
<script>
  import { MediumModal, ModalButton } from "flowbite-svelte";

  let modal1;
  let modal2;

  const handlebtnM1 = () => {
    modal1.closeModal()
  };

  const handlebtnM2 = () => {
    modal2.closeModal()
  };
  const handlebtnM3 = () => {
    modal2.closeModal()
  };
</script>
```

<h2 class="text-2xl w-full dark:text-white py-8">Examples</h2>

<div class="container flex flex-wrap justify-center rounded-xl mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
  <ModalButton id="modal1" btnName="Medium Modal" />
</div>

<MediumModal id="modal1" title="Basic Modal Title">
  Basic Modal Content: Lorem ipsum dolor sit, amet consectetur adipisicing
  elit. Ad odit aspernatur minus deserunt illo error eum temporibus officiis.
  Ab facere dolorem quisquam omnis? Aspernatur, asperiores voluptas quis culpa
  consectetur saepe!
</MediumModal>

<p class="dark:text-white py-4 text-lg"> Create a button and modal.</p>

```html
<ModalButton id="modal1" btnName="Medium Modal" />
<MediumModal id="modal1" title="Basic Modal Title">
  Basic Modal Content: Lorem ipsum dolor sit, amet consectetur adipisicing elit.
  Ad odit aspernatur minus deserunt illo error eum temporibus officiis. 
</MediumModal>
```

<h2 class="text-2xl w-full dark:text-white py-8">Medium Modals with an Action Button</h2>

<div class="container flex flex-wrap justify-center rounded-xl mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
  <ModalButton id="id1" btnName="Medium Modal with one action button" btnColor="gray" />
</div>

<MediumModal
  bind:this={modal1}
  id="id1"
  btnColor="yellow"
  title="Medium Modal Title"
  btn1="Close"
  on:handlebtn1={handlebtnM1}
>
  Modal 2 Content: Lorem ipsum dolor sit, amet consectetur adipisicing elit.
  Ad odit aspernatur minus deserunt illo error eum temporibus officiis. Ab
  facere dolorem quisquam omnis? Aspernatur, asperiores voluptas quis culpa
  consectetur saepe!
</MediumModal>

```html
<ModalButton id="id1" btnName="Medium Modal with one action button" btnColor="gray" />
<MediumModal
  bind:this={modal1}
  id="id1"
  btnColor="yellow"
  title="Medium Modal Title"
  btn1="Close"
  on:handlebtn1={handlebtnM1}
>
  Modal 2 Content: Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ad
  odit aspernatur minus deserunt illo error eum temporibus officiis. 
</MediumModal>
```

<h2 class="text-2xl w-full dark:text-white py-8">Medium Modals with action buttons</h2>

<div class="container flex flex-wrap justify-center rounded-xl mx-auto bg-gradient-to-r bg-white dark:bg-gray-900 border border-gray-200 dark:border-gray-700 p-2 sm:p-6">
  <ModalButton id="id2" btnName="Medium Modal with two action buttons" btnColor="blue" />
</div>

<MediumModal
  bind:this={modal2}
  id="id2"
  btnColor="indigo"
  title="Default Modal Title"
  btn1="Go home"
  btn2="Close"
  on:handlebtn1={handlebtnM2}
  on:handlebtn2={handlebtnM3}
>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
  tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
  quis nostrud exercitation ullamco.
</MediumModal>


```html
<ModalButton id="id2" btnName="Medium Modal with two action buttons" btnColor="blue" />
<MediumModal
  bind:this={modal2}
  id="id2"
  btnColor="indigo"
  title="Default Modal Title"
  btn1="Go home"
  btn2="Close"
  on:handlebtn1={handlebtnM2}
  on:handlebtn2={handlebtnM3}
>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor.
</MediumModal>
```

<h2 class="text-2xl w-full dark:text-white py-8">Props</h2>

<p class="dark:text-white py-4 text-lg">The component has the following props, type, and default values:</p>

```js
type Colors = 'blue' | 'gray' | 'red' | 'yellow' | 'purple' | 'green' | 'indigo' | 'pink';
let id = 'medium-modal';
let btnColor: Colors = 'blue';
let textColor: Colors = 'gray';
let title = 'Terms of Service';
let btn1: string;
let btn2: string;
const closeModal = () => {
  modalIdStore.update((value) => (value = null));
};
```