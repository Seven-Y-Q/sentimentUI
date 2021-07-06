<script>
  // core components
  import Table from "components/Cards/Table.svelte";
  import users from "../../data/users.js";
  export let location;

  const headers = [
    "OPEN_ID",
    "BIND_DATE",
    "BIND_STATUS",
    "CUSTOMER_ID",
    "PROD_ID"
  ];

  const data = users.data;
</script>

<div class="flex flex-wrap mt-4">
  <div class="w-full mb-12 px-4">
    <Table headers={headers} data={data} title="Customers" />
  </div>
</div>
