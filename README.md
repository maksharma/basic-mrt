# basic-mrt
basic server for mrt path finder

## API 1: (without time constrain)
Request :
```bash
curl --location --request GET 'localhost:3000/path' \
--header 'Content-Type: application/json' \
--data-raw '{
    "from": "Telok Blangah",
    "to": "Tanjong pagar"
}'```
Response:

```bash
{
    "count": 4,
    "routes": [
        {
            "title": "Route from TELOK BLANGAH to TANJONG PAGAR",
            "stops": 3,
            "steps": [
                "take CC line from TELOK BLANGAH towards HARBOURFRONT",
                "ride 1 stops on CC line to reach HARBOURFRONT",
                "change from CC line to NE line at HARBOURFRONT",
                "take NE line from HARBOURFRONT towards OUTRAM PARK",
                "ride 1 stops on NE line to reach OUTRAM PARK",
                "change from NE line to EW line at OUTRAM PARK",
                "take EW line from OUTRAM PARK towards TANJONG PAGAR",
                "ride 1 stops on EW line to reach TANJONG PAGAR"
            ],
            "meta": "[{\"line\":\"CC\",\"from\":\"CC28\",\"fromName\":\"TELOK BLANGAH\",\"to\":\"CC29\",\"toName\":\"HARBOURFRONT\",\"stops\":1},{\"line\":\"NE\",\"from\":\"NE1\",\"fromName\":\"HARBOURFRONT\",\"to\":\"NE3\",\"toName\":\"OUTRAM PARK\",\"stops\":1},{\"line\":\"EW\",\"from\":\"EW16\",\"fromName\":\"OUTRAM PARK\",\"to\":\"EW15\",\"toName\":\"TANJONG PAGAR\",\"stops\":1}]"
        },
        {
            "title": "Route from TELOK BLANGAH to TANJONG PAGAR",
            "stops": 8,
            "steps": [
                "take CC line from TELOK BLANGAH towards HARBOURFRONT",
                "ride 1 stops on CC line to reach HARBOURFRONT",
                "change from CC line to NE line at HARBOURFRONT",
                "take NE line from HARBOURFRONT towards DHOBY GHAUT",
                "ride 4 stops on NE line to reach DHOBY GHAUT",
                "change from NE line to NS line at DHOBY GHAUT",
                "take NS line from DHOBY GHAUT towards CITY HALL",
                "ride 1 stops on NS line to reach CITY HALL",
                "change from NS line to EW line at CITY HALL",
                "take EW line from CITY HALL towards TANJONG PAGAR",
                "ride 2 stops on EW line to reach TANJONG PAGAR"
            ],
            "meta": "[{\"line\":\"CC\",\"from\":\"CC28\",\"fromName\":\"TELOK BLANGAH\",\"to\":\"CC29\",\"toName\":\"HARBOURFRONT\",\"stops\":1},{\"line\":\"NE\",\"from\":\"NE1\",\"fromName\":\"HARBOURFRONT\",\"to\":\"NE6\",\"toName\":\"DHOBY GHAUT\",\"stops\":4},{\"line\":\"NS\",\"from\":\"NS24\",\"fromName\":\"DHOBY GHAUT\",\"to\":\"NS25\",\"toName\":\"CITY HALL\",\"stops\":1},{\"line\":\"EW\",\"from\":\"EW13\",\"fromName\":\"CITY HALL\",\"to\":\"EW15\",\"toName\":\"TANJONG PAGAR\",\"stops\":2}]"
        },
        {
            "title": "Route from TELOK BLANGAH to TANJONG PAGAR",
            "stops": 8,
            "steps": [
                "take CC line from TELOK BLANGAH towards HARBOURFRONT",
                "ride 1 stops on CC line to reach HARBOURFRONT",
                "change from CC line to NE line at HARBOURFRONT",
                "take NE line from HARBOURFRONT towards DHOBY GHAUT",
                "ride 4 stops on NE line to reach DHOBY GHAUT",
                "change from NE line to NS line at DHOBY GHAUT",
                "take NS line from DHOBY GHAUT towards RAFFLES PLACE",
                "ride 2 stops on NS line to reach RAFFLES PLACE",
                "change from NS line to EW line at RAFFLES PLACE",
                "take EW line from RAFFLES PLACE towards TANJONG PAGAR",
                "ride 1 stops on EW line to reach TANJONG PAGAR"
            ],
            "meta": "[{\"line\":\"CC\",\"from\":\"CC28\",\"fromName\":\"TELOK BLANGAH\",\"to\":\"CC29\",\"toName\":\"HARBOURFRONT\",\"stops\":1},{\"line\":\"NE\",\"from\":\"NE1\",\"fromName\":\"HARBOURFRONT\",\"to\":\"NE6\",\"toName\":\"DHOBY GHAUT\",\"stops\":4},{\"line\":\"NS\",\"from\":\"NS24\",\"fromName\":\"DHOBY GHAUT\",\"to\":\"NS26\",\"toName\":\"RAFFLES PLACE\",\"stops\":2},{\"line\":\"EW\",\"from\":\"EW14\",\"fromName\":\"RAFFLES PLACE\",\"to\":\"EW15\",\"toName\":\"TANJONG PAGAR\",\"stops\":1}]"
        },
        {
            "title": "Route from TELOK BLANGAH to TANJONG PAGAR",
            "stops": 8,
            "steps": [
                "take CC line from TELOK BLANGAH towards HARBOURFRONT",
                "ride 1 stops on CC line to reach HARBOURFRONT",
                "change from CC line to NE line at HARBOURFRONT",
                "take NE line from HARBOURFRONT towards DHOBY GHAUT",
                "ride 4 stops on NE line to reach DHOBY GHAUT",
                "change from NE line to NS line at DHOBY GHAUT",
                "take NS line from DHOBY GHAUT towards CITY HALL",
                "ride 1 stops on NS line to reach CITY HALL",
                "change from NS line to EW line at CITY HALL",
                "take EW line from CITY HALL towards TANJONG PAGAR",
                "ride 2 stops on EW line to reach TANJONG PAGAR"
            ],
            "meta": "[{\"line\":\"CC\",\"from\":\"CC28\",\"fromName\":\"TELOK BLANGAH\",\"to\":\"CC29\",\"toName\":\"HARBOURFRONT\",\"stops\":1},{\"line\":\"NE\",\"from\":\"NE1\",\"fromName\":\"HARBOURFRONT\",\"to\":\"NE6\",\"toName\":\"DHOBY GHAUT\",\"stops\":4},{\"line\":\"NS\",\"from\":\"NS24\",\"fromName\":\"DHOBY GHAUT\",\"to\":\"NS25\",\"toName\":\"CITY HALL\",\"stops\":1},{\"line\":\"EW\",\"from\":\"EW13\",\"fromName\":\"CITY HALL\",\"to\":\"EW15\",\"toName\":\"TANJONG PAGAR\",\"stops\":2}]"
        }
    ]
}
```