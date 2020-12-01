循环查询

```
declare @productId varchar(50)
declare my_c cursor
for (select a.productId from 
		(
		select c.itemPriceAmount,c.commodityId,p.disPrice,p.productId from HOMEDEPOT_COMMODITY_INFORMATION c,DA_PRODUCT p where c.productId = p.productId 
		) a group by a.productId
	)
open my_c;
fetch next from my_c into @productId;
while @@FETCH_STATUS = 0
	begin
		select productId,disPrice from DA_PRODUCT where productId = @productId;
		fetch next from my_c into @productId;
	end	
close my_c;
deallocate my_c;
GO

```

