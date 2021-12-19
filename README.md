# customer-rating-system
install nodejs
$ git clone git@github.com:nams05/rating-system.git
$ cd rating-system
$ npm install
$ npm start
rate a product
$ Send a POST request to http://35.238.38.7:80/ratings/rateProduct
$ Request: JSON
    {
        "productId":1,
        "customerId":10,
        "rating": 5
    }
$ Returns a Respose:JSON
    {
        "status": "success",
        "productRating": {
            "productId": 1,
            "customerId": 10,
            "rating": 5
        }
    }
    delete rating
    $ Send a POST request to http://35.238.38.7:80/ratings/remove
$ Request: JSON
    {
        "productId":1,
        "customerId":10
    }
$ Returns a Response: JSON
    {
        "status": "success",
        "productRating": {
            "productId": 1,
            "customerId": 10,
            "rating": 5
        }
    }
    fetch product rating id 1
    $ Send a GET request to http://35.238.38.7:80/ratings/getAverage/1
$ Returns a Response: JSON
    {
        "status": "success",
        "averageProductRating": {
            "productId": 1,
            "rating": 4.2
        }
    }
    fetch customer id 10
    $ Send a GET request to http://35.238.38.7:80/ratings/getByCustomer/10/1
$ Returns a Response: JSON
    {
        "status": "success",
        "productRating": {
            "productId": 1,
            "customerId": 10,
            "rating": 5
        }
    }
    fetch breakup rating
    $ Send a GET request to http://35.238.38.7:80/ratings/getAverage/1
$ Returns a Response: JSON
    {
        "status": "success",
        "averageProductRating": {
            "productId": 1,
            "rating": 4.2
        }
    }
