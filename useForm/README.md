# useForm Hook

Example:

``` 
  const initialForm = {
    searchForm: ""
  }
  
  const [formValues, handleInputChange, reset] = useForm(initialForm)
  const {searchForm} = formValues

  const handleSubmit = e=> {
    e.preventDefault()
    console.log(searchForm)
  }
  .
  .
  .
  <form onSubmit={handleSubmit}>
    <input
      type="text"
      placeholder="Find your hero"
      className="form-control"
      name="searchForm"
      value={searchForm}
      onChange={handleInputChange}
    />
    <button className="btn btn-outline-primary mt-3 btn-block">Search...</button>
  </form>
  
```