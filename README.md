# ASP.NET-Tutorial
 
// Khởi tạo project

dotnet new webapi -o api

dotnet watch run

// download nuget

Microsoft.EntityFrameworkCore.SqlServer
Microsoft.EntityFrameworkCore.Design
Microsoft.EntityFrameworkCore.Tools

//Tạo Migrations

dotnet ef migrations add init
dotnet ef database update

//appsettings.json

"ConnectionStrings": {
    "DefaultConnection": "Data Source=(local);Initial Catalog=YOURDATABASE;User ID=sa;Password=123;Trusted_Connection=True;Trust Server Certificate=True"
}
*Lưu ý: Phải thay đổi từ true sang false trong file .csproj
<InvariantGlobalization>false</InvariantGlobalization>


*Lưu ý: Khi tạo controller thì phải khai báo vào trong Program.cs {
	builder.Services.AddControllers();
	app.MapControllers();
}
*Lưu ý: Khi nào sử dụng interface repo thì phải add scope ở Program.cs {
builder.Services.AddScoped<IStockRepository, StockRepository>();
}
