<script>
  import { setContext } from "svelte";
  import Navbar from "./Navbar.svelte";
  import ExpensesList from "./ExpensesList.svelte";
  // data
  import expensesData from "./expenses";
  // variables
  let expenses = [...expensesData];
  function removeExpense(id) {
    expenses = expenses.filter((item) => item.id !== id);
  }
  setContext("remove, removeExpense")
</script>

<!-- <style></style> -->
<!-- CSS/STYLING -->

<Navbar />
<main class="content">
  <ExpensesList {expenses} />
</main>
