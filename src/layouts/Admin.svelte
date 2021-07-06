<script>
  import { Router, Route } from "svelte-routing";

  // components for this layout
  import AdminNavbar from "components/Navbars/AdminNavbar.svelte";
  import Sidebar from "components/Sidebar/Sidebar.svelte";
  import HeaderStats from "components/Headers/HeaderStats.svelte";
  import FooterAdmin from "components/Footers/FooterAdmin.svelte";

  // pages for this layout
  import Dashboard from "views/admin/Dashboard.svelte";
  import Settings from "views/admin/Settings.svelte";
  import Product from "views/admin/Product.svelte";
  // import Comment from "views/admin/Comment.svelte";
  import User from "views/admin/User.svelte";
  import Followers from "views/admin/Followers.svelte";
  import Articles from "views/admin/Articles.svelte";
  import ArticlesByProd from "views/admin/ArticlesByProd.svelte";
  import CommentsByArticle from "views/admin/CommentsByArticle.svelte";
  import CommentsByUser from "views/admin/CommentsByUser.svelte";
  import UserProdMatrix from "views/admin/UserProdMatrix.svelte";

  export let location;
  export let admin = "";
</script>

<div>
  <Sidebar location={location}/>
  <div class="relative md:ml-64 bg-blueGray-100">
    <HeaderStats />
    <div class="px-4 md:px-10 mx-auto w-full -m-24">
      <Router url="admin">
        <Route path="dashboard" component="{Dashboard}" />
        <Route path="settings" component="{Settings}" />
        <Route path="product" component="{Product}" />
        <Route path="product/:aid" component="{ArticlesByProd}" />
        <Route path="product/:aid/:cid" component="{CommentsByArticle}" />
        <Route path="user" component="{User}" />
        <Route path="user/:oid" component="{CommentsByUser}" />
        <Route path="followers" component="{Followers}" />
        <Route path="articles" component="{Articles}" />
        <Route path="customerProdMatrix" component="{UserProdMatrix}" />
      </Router>
    </div>
  </div>
</div>
