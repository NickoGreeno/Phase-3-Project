# Phase-3-Project

<html>
    <body>
        <h2>Overview</h2>
        <p>This project analyzes car crashes in Chicago to create a classification model that is able to predict injury in
           event of a car crash.The information found could be useful for insurance agencies that have
           to deal with claims. A common issue insurance companies face is fraud, and therefore an AI that can either confirm
           or deny will help with that and lead to more genuine insurance cases.
        </p>
    </body>
          
<body>
    <h2> Business Understanding </h2>
    <p> Insurance companies commonly use statistics in determining insurance rates. When there are greater claims than expected there arises 
        a natural suspicion of fraud. The goal of this project is tocreate an algorithm that uses data collected from Chicago, 
        in order to determine whether an injury took placein event of a car crash. This AI with its ability should expect to mirror 
        the true population of injuries of whicheverarea it is predicting. Therefore in this example of Chicago, if the AI is accurate, 
        the distribution of injury orno injury should emulate the true population of individuals who were truly injured in a car crash.
    </p>
    <img src="https://www.moneycrashers.com/wp-content/uploads/2016/09/chicago-illinois-traffic-810x455.jpg" 
         alt="Chicago Illinois Traffic" width="600" height="180">
    <p> After establishing an optimal AI, I will market the findings to car insurance company Progressive. They will be able
        to better establish insurance rates by finding the true rate of injury which will lower fraud and therefore unneeded payouts.
    </p>
    </body>

<body>
    <h2> Modeling </h2>
    <p> I started with a logistic model since they are a simple classifier model.</p>
    <p> After that, I set up a gridsearch model using a pipeline that uses a DecisionTreeClassifier.<br>
        My reasoning for that was to start parameter tuning while also delving into a smarter model.
    </p>
    <p> I then instantiated a normal XGB model because they use their internal gradient function to search for the optimal settings, 
        I figured it was a natural step after a DecisionTree. When I was finished with that, I set a gridsearchinh XGB model.
        It was my thought of putting the last two models I made together to get the best of both worlds. The model iterated
        through my grid to establish its own best parameters.
    </p>
    
<body>
    <h2> Model Evaluation </h2>
        <hr>
        <p> In order to evaluate how well each model performed, I looked at their Recall and Accuracy scores.
            <br>
            <br>
            I did this since the Recall metric is a measurement of how well the model finds the postive samples.
            That is is especially important in this case since I am trying to find when injury truly occured. Also, in the
            real world application, an instance where a false negative is reported is ultimately worse than a false positive.
            <br>
            <br>
            The accuracy score will be a reflection of the overall performance of the model. This is still important to
            consider since the goal of the project is to use the model for scrutinizing insurance claims.
        </p>
    </body>
    

<body>
    <h2> How I conducted model testing:</h2>
        <p> After instiantiating the models, I ran a code that ran the model that then shared the model's grading metrics for their train,
            and test data. Resized samplings using SMOTE were also included.
        </p>
    <p> The models being stochastic in nature provided different results when I would run the same code.
        To address that, I made a code that ran the ModelSummary function n number of times. After setting n to 5, I ran all
        of my models that many times. I ended up choosing the <b>gridsearch</b> model because its recall and accuracy score were the most 
        consistent and well performing of the models. It also did not run for too long, especially when comparing to the XGB grid model.
    </p>
</body>
    