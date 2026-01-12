# dotnet-webapi-sample
This is a sample RESTful Web API built using ASP.NET Core, following clean architecture and best practices for enterprise applications. - C# - ASP.NET Core - Entity Framework Core - SQL Server - Swagger 

//
[ApiController]
[Route("api/products")]
public class ProductsController : ControllerBase
{
    private readonly IProductService _service;

    public ProductsController(IProductService service)
    {
        _service = service;
    }

    [HttpGet]
    public async Task<IActionResult> GetAll()
    {
        return Ok(await _service.GetAllAsync());
    }
}
//
