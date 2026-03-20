"what error am i encountering in this  <h1>Cash Flow</h1>
    <form>
        <label for="total-salary">Total Salary :</label>
        <input type="number" id="total-salary" name="total-salary"/>
        <br/>
        <br/>
        <label for="expense-name">Expense Name :</label>
        <input type="text"  id="expense-name" name="expense-name"/>
        <br/>
        <br/>
        <label for="expense-amount">Expense Amount :</label>
        <input type="number" id="expense-amount" name="expense-amount"/>
        <br/>
        <br/>
        <button type="submit" onclick="displaySalary();">Add</button>
    </form>

    <h3>Total Salary :</h3>
    <p id="salary"></p>
    <h3>Remaining Balance :</h3>
    <script>
        function displaySalary(){
            event.preventDefault();
            let totalSalary = document.getElementById('total-salary').value();
            let displayedSalary = document.getElementById('salary');
            displayedSalary.innerText()=totalSalary;
            // console.log(totalSalary);
"

"how can i continue adding items in list while keeping th old items intact
function displaySalary(event){
            event.preventDefault();
            let totalSalary = document.getElementById('total-salary').value;
            let expenseName = document.getElementById('expense-name').value;
            let expenseAmount = document.getElementById('expense-amount').value;
            if (expenseAmount<=0){
                alert('Only positive expenses greater than 0 is accepted. Re-enter Expense Amount.')
            }
            else{
            document.getElementById('expense-list').innerHTML=`<li>${expenseName} : ${expenseAmount}</li>`;
            }
            document.getElementById('salary').innerText=totalSalary;
            document.getElementById('balance').innerText=totalSalary-expenseAmount;
        }
"