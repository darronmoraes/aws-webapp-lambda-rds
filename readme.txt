async function submitMe(){
            let firstName = document.getElementById("firstName").value;
            let lastName = document.getElementById("lastName").value;
            let salary = document.getElementById("salary").value;
            console.log({firstName: firstName, lastName: lastName, salary: salary, axios: document});
        }


        onclick="submitMe()"

<script type="text/javascript">
        function submitData() {
            var apigClientFactory = require('aws-api-gateway-client').default;
            var apigClient = apigClientFactory.newClient();
        let firstname = document.getElementById("firstname").value;
        let lastname = document.getElementById("lastname").value;
        let salary = document.getElementById("salary").value;

        var params = {
    //This is where any header, path, or querystring request params go. The key is the parameter named as defined in the API
    param0: '',
    param1: ''
};
var body = {
    //This is where you define the body of the request
    firstname, lastname, salary
};
var additionalParams = {
    //If there are any unmodeled query parameters or headers that need to be sent with the request you can add them here
    headers: {
        param0: '',
        param1: ''
    },
    queryParams: {
        param0: '',
        param1: ''
    }
};

apigClient.post({}, body, { headers: { 'Content-Type': 'application/json'}})
    .then(function(result){
        //This is where you would put a success callback
        console.log({result});
    }).catch( function(result){
        //This is where you would put an error callback
        console.log({errorResult: result});
    });
        }

        
</script>