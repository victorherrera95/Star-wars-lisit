<template>
  	<div id="app">
    	<div class="container-fluid">
			<Header></Header>
			<Loading v-show="loadingStatus"></Loading>
			<Search v-show="!loadingStatus"></Search>
			<OrderBy v-show="!loadingStatus"></OrderBy>
      		<Movies v-show="!loadingStatus"></Movies>
			<Pagination v-show="!loadingStatus"></Pagination>
    	</div>
  	</div>
</template>

<script>
import { mapState } from "vuex";
import Header from "./components/Header"
import Loading from "./components/Loading"
import Search from "./components/Search"
import OrderBy from "./components/OrderBy"
import Movies from "./components/Movies"
import Pagination from "./components/Pagination"

export default {
  	name: "app",
  	components: {
		Header,
		Loading,
		Search,
		OrderBy,
		Movies,
		Pagination,
  	},
  	computed: {
    	...mapState(["loadingStatus"])
	}
};
</script>