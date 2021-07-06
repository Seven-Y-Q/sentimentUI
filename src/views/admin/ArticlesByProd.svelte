<script>
  // core components
  import Table from "components/Cards/Table.svelte";
  import articlesByProd from "../../data/articlesByProd.js";
  export let location;
  export let aid;

  const headers = [
    "SHARE_USER",
    "ADD_TO_FAV_COUNT",
    "MSG_ID",
    "SHARE_COUNT",
    "REF_PROD",
    "CREATE_DATE",
    "TARGT_USER",
    "READ_COUNT",
    "READ_USER",
    "TITLE",
    "ADD_TO_FAV_USER"
  ];

  const data = articlesByProd.data;
</script>

<div class="flex flex-wrap mt-4">
  <div class="w-full mb-12 px-4">
    <Table headers={headers} data={data} id={aid} title="Articles by Product id" />
  </div>
</div>
