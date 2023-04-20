<template>
  <div
    class="item mt-8 flex before:border-l-divider-light-2 after:border-l-divider-light-2 before:dark:border-l-divider-dark-2 after:dark:border-l-divider-dark-2 lg:mt-0 lg:before:absolute lg:before:-left-1 lg:before:block lg:before:border-l lg:after:absolute lg:after:-left-1 lg:after:block lg:after:border-l"
  >
    <i
      class="flex h-8 w-8 place-content-center place-items-center border-divider-light-2 text-light-1 dark:border-divider-dark-1 dark:text-dark-2 lg:absolute lg:-left-7 lg:h-12 lg:w-12 lg:rounded-lg lg:border lg:border-divider-light-2 lg:bg-white lg:dark:border-divider-dark-2 lg:dark:bg-black"
    >
      <slot name="icon"></slot>
    </i>

    <div class="ml-4 flex-1">
      <h3 class="mb-2 text-sm font-medium text-light-1 dark:text-dark-2">
        <slot name="heading"></slot>
      </h3>

      <slot></slot>
    </div>
  </div>
</template>

<style scoped>
@media (min-width: 1024px) {
  .item {
    padding: 0.4rem 0 1rem calc(80px / 2);
  }

  i {
    top: calc(50% - 25px);
  }

  .item:before {
    bottom: calc(50% + 25px);
    height: calc(50% - 25px);
  }

  .item:after {
    top: calc(50% + 23px);
    height: calc(50% - 23px);
  }
}
</style>
