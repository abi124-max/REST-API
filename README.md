# REST-API
**company**:CODTECH IT SOLUTION PVT.LTD
**NAME**:H.Abirami
**INTERN ID**:CT08GNX
**DOMAIN**:JAVA programming
**BATCH DURATION**:25-12-24 to 25-01-25
**MENTOR NAME**:NEELA SANTHOSH
# ENTER THE DESCRIPTION  OF TASK PERFORMED WITHIN 500 WORDS
REST (Representational State Transfer) is an architectural style for designing networked applications. It relies on a stateless, client-server, cacheable communications protocol -- the HTTP. RESTful applications use HTTP requests to perform CRUD (Create, Read, Update, Delete) operations on resources.
Resources: In REST, resources are identified by URIs (Uniform Resource Identifiers). Each resource can be represented in different formats, such as JSON, XML, or HTML.
HTTP Methods: RESTful APIs use standard HTTP methods to perform operations on resources:
GET: Retrieve a resource.
POST: Create a new resource.
PUT: Update an existing resource.
DELETE: Remove a resource.
# PROGRAM
import java.io.BufferedReader;
import java.io.InputStream;
import java.io.InputStreamReader;
import java.io.OutputStream;
import java.net.HttpURLConnection;
import java.net.URL;

public class RestConsumer {
    public static void main(String[] args) {
        try {
            URL url = new URL("https://jsonplaceholder.typicode.com/todos/1");
            HttpURLConnection conn = (HttpURLConnection)url.openConnection();
            conn.setDoOutput(true);
            conn.setRequestMethod("GET");
            conn.setRequestProperty("Content-Type", "application/json");

            InputStream in = conn.getInputStream();
            BufferedReader br = new BufferedReader(new InputStreamReader(in));
            String output;
            System.out.println("Response from REST API:");
            while ((output = br.readLine()) != null) {
                System.out.println(output);
            }
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
# output





