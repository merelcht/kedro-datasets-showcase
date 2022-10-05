
<template>
  <div class="slidev-layout two-columns w-full h-full grid grid-cols-2 pt-0 pb-0">
    <div class="col-left mt-10">
      <slot />
    </div>
    <div class="col-right">
        <iframe id=scaled-frame src="https://demo.kedro.org" title="Kedro Demo"></iframe>
    </div>
  </div>
</template>
