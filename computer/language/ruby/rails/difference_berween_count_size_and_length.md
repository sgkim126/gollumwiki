# count, size, length의 차이
## count
 * 언제나 db에서 count를 가져온다.
## size
 * collection이 load되어 있으면, collection의 size를 가져온다.
 * collection이 load되어 있지 않으면, db에서 count를 가져온다.
## length
 * size를 호출한다.
