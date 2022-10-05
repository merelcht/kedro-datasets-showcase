
<template>
  <div class="slidev-layout two-columns w-full h-full grid grid-cols-2 pt-0">
    <div class="col-left mt-10">
      <slot />
    </div>
    <div class="col-right">
        <iframe id=scaled-frame src="https://demo.kedro.org" title="Iframe Example"></iframe>
    </div>
  </div>
</template>
