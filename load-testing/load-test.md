
## Config Details

    config:
      target: 'http://localhost:3010'
      http:
        pool: 50
      phases:
        - duration: 240
          arrivalRate: 10
    scenarios:
      - flow:
          - loop:
            - get:
                url: "/?id={{$randomNumber(1,10000000)}}"
            count: 200



## Sample Results

    Summary report @ 10:36:16(-0700) 2020-07-18
      Scenarios launched:  2400
      Scenarios completed: 2400
      Requests completed:  480000
      Mean response/sec: 1305.66
      Response time (msec):
        min: 0.8
        max: 1241.1
        median: 645.8
        p95: 1050.6
        p99: 1137.6
      Scenario counts:
        0: 2400 (100%)
      Codes:
        200: 480000