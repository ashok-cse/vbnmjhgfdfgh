/ 
 <script  >
 export let open = false;

 import {
    Dialog,
    DialogOverlay,
    PopoverOverlay,
    TransitionChild,
    TransitionRoot,
  } from '@rgossiaux/svelte-headlessui';
 </script>

 <TransitionRoot as="div" show={open} >
     <Dialog as="div" class="fixed inset-0 z-40" on:close={() => (open = false)} static>
      <TransitionChild
        as="div"
        enter="transition-opacity ease-linear duration-200"
        enterFrom="opacity-0"
        enterTo="opacity-100"
        leave="transition-opacity ease-linear duration-200"
        leaveFrom="opacity-100"
        leaveTo="opacity-0"
      >
        <DialogOverlay class="fixed inset-0 bg-black bg-opacity-25" />
      </TransitionChild>
      <TransitionChild
        as="div"
        enter="transition ease-linear duration-200 transform"
        enterFrom=" -translate-x-full opacity-0 "
        enterTo="opacity-100 translate-x-0"
        leave=" transition transition-opacity ease-linear duration-200 transform"
        leaveFrom="opacity-100 translate-x-0"
        leaveTo="opacity-0 -translate-x-full"
        class="w-full h-full"
      >
      <div class="w-full h-full bg-blue-500">
      fgfasdfasdfasdf
      </div>

     </TransitionChild>
    </Dialog>
  </TransitionRoot>