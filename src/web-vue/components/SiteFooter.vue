<script setup lang="ts">
import mark from "../assets/ae-mark-small.svg";
import markReversed from "../assets/ae-mark-small-reversed.svg";
</script>

<template>
  <footer class="foot">
    <div class="row">
      <a class="credit" href="https://appliedentropy.dev" target="_blank" rel="noopener">
        <img class="mark light" :src="mark" alt="" width="20" height="24" />
        <img class="mark dark" :src="markReversed" alt="" width="20" height="24" />
        An Applied Entropy project
      </a>
      <ul class="links">
        <li><a href="https://pimusic.stream" target="_blank" rel="noopener">Docs</a></li>
        <li><a href="https://github.com/mintopia/encore" target="_blank" rel="noopener">Source</a></li>
        <li><a href="https://github.com/mintopia/encore/issues" target="_blank" rel="noopener">Issues</a></li>
        <li><a href="https://github.com/mintopia/encore/blob/develop/LICENSE" target="_blank" rel="noopener">MIT licence</a></li>
      </ul>
    </div>
  </footer>
</template>

<style scoped>
.foot { border-top: 1px solid var(--line2); font-size: 13px; line-height: 1.5; color: var(--faint); }
.row { display: flex; flex-wrap: wrap; align-items: center; gap: 12px 24px; max-width: 1200px; margin: 0 auto; padding: 24px; }
.foot a { color: inherit; font-weight: 500; text-decoration: none; }
.foot a:hover { color: var(--txt); text-decoration: underline; }
.credit { display: flex; align-items: center; gap: 8px; margin-right: auto; }
.mark { display: block; height: 24px; width: auto; }
.mark.dark { display: none; }
:root[data-theme="dark"] .mark.light { display: none; }
:root[data-theme="dark"] .mark.dark { display: block; }
.links { display: flex; flex-wrap: wrap; gap: 8px 16px; margin: 0; padding: 0; list-style: none; }
@media (max-width: 719px) { .row { flex-direction: column; align-items: flex-start; } }
</style>
