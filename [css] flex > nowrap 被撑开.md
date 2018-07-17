```less
.flex{
  .fx1{
    flex: 1,
    min-width: 0; // **加上这个
    .text{
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
    }
  }
}
```
