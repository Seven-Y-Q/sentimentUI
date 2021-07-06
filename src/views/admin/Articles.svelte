<script>
  // core components
  import Table from "components/Cards/Table.svelte";
  import articles from "../../data/articles.js";
  export let location;

  const headers = [
    "MSG_ID",
    "REF_PROD",
    "TITLE",
    "TARGT_USER",
    "READ_USER",
    "READ_COUNT",
    "SHARE_USER",
    "SHARE_COUNT",
    "ADD_TO_FAV_COUNT",
    "ADD_TO_FAV_USER"
  ];

  const data = articles.data;
</script>

<div class="flex flex-wrap mt-4">
  <div class="w-full mb-12 px-4">
    <Table headers={headers} data={data} title="Articles" />
  </div>
</div>
