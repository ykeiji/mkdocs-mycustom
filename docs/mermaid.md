# mermaid サンプル

#### Mermaid Official document
[https://mermaid.js.org/syntax/flowchart.html](https://mermaid.js.org/syntax/flowchart.html)

## Flowchart

```mermaid
flowchart LR
A --> B
B --> C
C --> A
```

```mermaid
flowchart LR
A == 太線 === B
A -. 点線 -.- C
A == 太い矢印 ==> D
A -. 点線矢印 .-> E
A -- 丸矢印 --o F
A -- x矢印 --x G
H <-->|双方向矢印| I
H x--x|双方向矢印| J
H o--o|双方向矢印| K
```

```mermaid
flowchart TB
c1-->a2
subgraph one
a1-->a2
end
subgraph two
b1-->b2
end
subgraph three
c1-->c2
end
```

```mermaid
graph LR
A((S1))--1/1-->B((S2))
B--1/1-->C((S3))
C--1/1-->A
A--0/0-->A
B--0/0-->B
C--0/0-->C
```

## Sequence
```mermaid
sequenceDiagram
    App ->>+ API: GET /user:id
    API ->>+ Server: auth
    Server->>-API: user-data
    alt 200
        API->>App:OK
    else 400
        API->>-App:error
    end
```
```mermaid
sequenceDiagram
    Alice ->> Bob: Hello Bob, how are you?
    Bob-->>John: How about you John?
    Bob--x Alice: I am good thanks!
    Bob-x John: I am good thanks!
    Note right of John: Bob thinks a long<br/>long time, so long<br/>that the text does<br/>not fit on a row.

    Bob-->Alice: Checking with John...
    Alice->John: Yes... John, how are you?
```

## ER diagram
```mermaid
erDiagram

    user{
        number user_id
        string user_name
    }

    follow{
        number follow_id
        number user_id
    }

    follower{
        number follower_id
        number user_id
    } 

    post{
        number post_id
        number user_id
        string title
        string text
        datetime posted_at
    }

    reply{
        number reply_id
        number reply_to
        number user_id
        string text
        datetime posted_at
    }

    user ||--o{ follow: ""
    user ||--o{ follower: ""
    user ||--o{ post: ""
    post ||--o{ reply: ""
```

## Gantt chart
```mermaid
gantt
    title Develop
    dateFormat YYYY-MM-DD

    section Develop
    Plan:a,2022-10-09 ,1m
    Design:b,after a ,1m
    Implement:c,after b ,2m
    QA:d,after c, 1m
    Release:e,after d, 1m
```

## Pie chart
```mermaid
%%{init: {"pie": {"textPosition": 0.5}, "themeVariables": {"pieOuterStrokeWidth": "5px"}} }%%
pie showData
    title Key elements in Product X
    "Calcium" : 42.96
    "Potassium" : 50.05
    "Magnesium" : 10.01
    "Iron" :  5
```

## Quadrant chart
```mermaid
quadrantChart
    title Reach and engagement of campaigns
    x-axis Low Reach --> High Reach
    y-axis Low Engagement --> High Engagement
    quadrant-1 We should expand
    quadrant-2 Need to promote
    quadrant-3 Re-evaluate
    quadrant-4 May be improved
    Campaign A: [0.3, 0.6]
    Campaign B: [0.45, 0.23]
    Campaign C: [0.57, 0.69]
    Campaign D: [0.78, 0.34]
    Campaign E: [0.40, 0.34]
    Campaign F: [0.35, 0.78]
```

## Mind map
```mermaid
mindmap
  root((mindmap))
    Origins
      Long history
      ::icon(fa fa-book)
      Popularisation
        British popular psychology author Tony Buzan
    Research
      On effectiveness<br/>and features
      On Automatic creation
        Uses
            Creative techniques
            Strategic planning
            Argument mapping
    Tools
      Pen and paper
      Mermaid
```

## Sankey diagram
```mermaid
sankey-beta

Bio-conversion,Losses,26.862

Bio-conversion,Solid,280.322

Bio-conversion,Gas,81.144

```

## Architecture diagram
```mermaid
architecture-beta
    group api(cloud)[API]

    service db(database)[Database] in api
    service disk1(disk)[Storage] in api
    service disk2(disk)[Storage] in api
    service server(server)[Server] in api

    db:L -- R:server
    disk1:T -- B:server
    disk2:T -- B:db

```