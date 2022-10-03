<!-- default.vue -->
<!-- <template>
  <div class="slidev-layout two-cols left">
    <slot />
    <iframe src="https://demo.kedro.org" height="200" width="300" title="Iframe Example"></iframe>
  </div>

</template> -->



<template>
  <div class="slidev-layout two-columns w-full h-full grid grid-cols-2">
    <div class="col-left">
      <slot />
    </div>
    <div class="col-right">
        <iframe id=scaled-frame src="https://demo.kedro.org" title="Iframe Example"></iframe>
    </div>
  </div>
</template>
