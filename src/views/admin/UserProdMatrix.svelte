<script>
  // core components
  import Table from "components/Cards/Table.svelte";
  import userProdMatrix from "../../data/userProdMatrix.js";
  export let location;

  const headers = [
    "User/Product",
    "1001",
    "1002",
    "1003",
    "1004",
    "1005",
    "1006",
    "1007",
    "1008",
    "1009"
  ];

  const data = Object.keys(userProdMatrix.data).map(item => ({ ...userProdMatrix.data[item], 'User/Product': item }));
</script>

<div class="flex flex-wrap mt-4">
  <div class="w-full mb-12 px-4">
    <Table headers={headers} data={data} title="User Product Matrix" />
  </div>
</div>
