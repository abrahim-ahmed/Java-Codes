import java.util.HashMap;
import java.util.List;
import java.util.Map;

public class SearchEngine {
    private Map<String, List<String>> searchIndex;

    public SearchEngine() {
        searchIndex = new HashMap<>();
    }

    public void indexDocument(String document, List<String> keywords) {
        for (String keyword : keywords) {
            if (searchIndex.containsKey(keyword)) {
                searchIndex.get(keyword).add(document);
            } else {
                searchIndex.put(keyword, new ArrayList<>(List.of(document)));
            }
        }
    }

    public List<String> search(String query) {
        List<String> results = new ArrayList<>();

        if (searchIndex.containsKey(query)) {
            results.addAll(searchIndex.get(query));
        }

        return results;
    }
}
